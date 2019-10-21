# Setup Instructions
## 1. Create new virtualenv :
python3 -m venv myenv 

OR 
virtualenv -p python3 env_name_here  

These are identical in Python3 for creating virtualenv.

cd your_env_name_here


## 2. Populate the /bin/activate script:
AWS_PROFILE="your_aws_profile_here"

export AWS_PROFILE


AND make the project to be a Python Package:

touch __init__.py

## 3. Edit the bash profile, e.g. gedit ~/.profile for command to activate the virtualenv
gedit ~/.profile

alias aws_start="cd /home/alari/dev/start_aws/aws_base_setup && source env_name_here/bin/activate"

source ~/.profile

## 4. Activate the virtualenv 
aws_start

## 5. Edit Makefile & Run the Installation and Test Scripts:
Edit Makefile to account for any changes in the paths

make all

# Known Issues
## Pip Client 404 Error
In this case, update PIP via curl https://bootstrap.pypa.io/get-pip.py | python3 
*before running any make commands*,

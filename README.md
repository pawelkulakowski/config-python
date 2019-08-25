### Git Installation
```
# Install Git
$ sudo apt install git

# Checking the installation
$ git --version

# Generate SSH Key
$ ssh-keygen -t rsa -b 4096 -C "krakowiakpawel9@gmail.com"
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_rsa

# Checking configuration
$ ssh -T git@github.com

# Clone existing repository
$ git clone "https://github.com/krakowiakpawel9/config-python.git"
```

### Python - Environment Management - Linux (Ubuntu)

```
# Run python
$ python3

# Display python path
$ which python3

# Display python path with sys package
$ python3
>>> import sys
>>> sys.executable

### Anaconda Installation
# Go to https://www.anaconda.com/distribution/
# Find the latest Linux version, download anr run bash script
$ bash Anaconda3-2019.07-Linux-x86_64.sh
# Default Location: /home/user/anaconda3
# Enter 'yes' two times during the installation
# Verify your installation
$ which python3


# Checking version
$ conda --version

# Update conda
$ conda update conda

# Display all environments 
$ conda env list
$ conda info --envs

# Display all available packages
$ conda list

# Create new environment with specific version of python
# Default location:
#    /home/user/anaconda3/envs/my_app
$ conda create --name my_app python=2.7

# Activate the environment
$ conda activate my_app

# List all packages in the environment
$ conda list

# Install package
$ conda install numpy
$ conda install -y numpy

# List all packages in the environment - checking installation 
$ conda list
$ conda list | grep numpy

# Remove package (deafult with dependencies)
$ conda remove numpy

# Remove only main package without dependencies
$ conda remove --force numpy

# Install many packages
$ conda install numpy pandas matplotlib

# Search for specific version
$ conda search numpy

# Install specific version
$ conda install numpy==1.16.0

# Remove an environment
$ conda remove --name my_app --all

# Make an exact copy of an environment
$ conda create --clone old_env --name new_env

# Export an environment to a YAML file that can be read on Windows, macOS, Linux
$ conda env export --name ENV_NAME > env_name.yml

# Create an environment from the YAML file
$ conda env create --file env_name.yml

```

### Data Science
```# Create virtual environment
$ conda create --name science python=3.6

# Install Jupyter Notebook
$ conda install -c anaconda jupyter
$ which jupyter

# Run Jupyter Notebook
$ jupyter-notebook

# Install Jupyter Lab
$ conda install -c conda-forge jupyterlab
$ which jupyter-lab

# Run Jupyter Lab
$ jupyter-lab

# Open Jupyter from the console
$ which jupyter
$ jupyter-notebook

# Install package from jupyter 
!conda install -y numpy

# Install Spyder
$ conda install -c anaconda spyder

# Run Spyder
$ spyder```
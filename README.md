# Assignment_egm722
Python script and data files for an assignment for module EGM722

## Set-up and Installation

In order to run the script, git and conda must first be installed on the computer being used. If this is not already the case, the git installer 
can be downloaded from the official [git website] (https://git-scm.com/install/windows). Click on whichever operating system your computer uses, 
and then follow the instructions provided. To install conda, the easiest way is to download and install Anaconda Navigator from its [official website] 
(https://www.anaconda.com/download/success). Again, select whichever operating system your computer uses, and follow the instructions.

Once these are installed, log in to your GitHub account if you have one. If not, you can sign up for a free account [here] (https://github.com/). 
If you want to use an integrated development environment (IDE) to run the script, PyCharm can be downloaded [here] (https://www.jetbrains.com/pycharm/download/). 
Please note, you will automatically be given one month of PyCharm Professional for free, but once this runs out, you will drop down to the basic 
version without any issues.
In order to work with the script, you need to fork the repository where it’s saved to your own git account, and then clone this fork. Forking a 
repository means that you copy an existing repository to your own account, and any changes you make to this copy do not affect the original, while 
cloning a repository makes a copy of it on your local machine that is synched to the version on your GitHub account – any changes made to the local 
copy get committed to the version on GitHub.

The script is found in the following repository [here](https://github.com/Keenan-T7/Assignment_egm722)

In order to fork this repository, follow the link above to it. In the top right corner of the page, there is a fork button. Click on it to be taken 
to a new page called “Create a new fork”. Then click on “Create Fork”.

To clone this, use the following command:

'git clone https://github.com/{username}/egm722/tree/main/Assignment.git'

If you haven’t got a GitHub account, you can use this command instead:

'git clone https://github.com/Keenan-T7/egm722/tree/main/Assignment.git'

Once this is done, you should set up a conda environment using the environment.yml file which can be found in the repository. If you have installed 
Anaconda Navigator, you can do this by clicking on Environments, then on Import, and then navigating to wherever you have cloned the repository to 
on your computer and selecting the environment.yml file. If you prefer to use a command prompt, use cd to move to the location of the repository on 
your computer, and then type in the following command

'conda env create -f environment.yml'

The environment file reads as follows:

name: egm722_assignment
channels:
  - conda-forge
  - defaults
dependencies:
  - python=3.9
  - geopandas
  - folium 

This will then define an environment called “egm722_assignment”, which uses conda-forge and defaults as its channels and has Python 3.9, 
[geopandas] (https://geopandas.org/en/stable/index.html) and [folium] (https://python-visualization.github.io/folium/latest/index.html) as its dependencies.

The data required for the script to work is included in the repository, in a folder called ‘data_files’. It contains shapefiles for three sets of 
administrative boundaries - Local Government Districts (LGDs), District Electoral Areas (DEAs), and Super Data Zones (SDZs) - and csv files of data 
for the same three administrative boundaries and for the nine Emergency Departments (EDs) in Northern Ireland. The script is initially set up to 
produce a map based on the DEA boundaries, but this can be changed to show one of the other two if required.

# CSci 574: Final Class Project

## Project Description

Please specify the data source you have selected and write a paragraph of what you hope to
do with the data you choose for the class project here.

## Project Structure

In general the directory structure for this project/class repository follows
suggestions and best practices for create data science projects.
See for example
[Cookie Cutter data science](https://drivendata.github.io/cookiecutter-data-science/)
and [Python data science projects](https://gist.github.com/ericmjl/27e50331f24db3e8f957d1fe7bbbe510)

Here is the overview of the class repository structure:

```
$ pwd
/path/to/local/repos/ml-python-class

$ tree
.
├── data
│   ├── data-file-1.csv
│   ├── data-file-2.csv
│   ├── ...
│   └── data-file-X.csv
├── docs
│   ├── csci574-sem-YEAR-syllabus.docx
│   └── csci574-sem-YEAR-syllabus.pdf
├── figures
│   ├── figure-01.png
│   ├── figure-02.png
│   ├── ...
│   └── figure-XX.png
├── lectures
│   ├── Lecture-01-name.ipynb
│   ├── Lecture-02-name.ipynb
│   ├── Lecture-02a-Numpy.ipynb
│   ├── ...
│   └── Lecture-XX-name.ipynb
├── scripts
│   ├── bootstrap-anaconda3-python.sh
│   ├── bootstrap-jupyterhub-server.sh
│   ├── bootstrap.sh
│   └── script-name.py
├── src
│   ├── ml_python_class
│   │   ├── custom_funcs.py
│   │   ├── __init__.py
│   └── setup.py
├── LICENSE
├── README.md
└── .devcontainer
```

**data/**

All data files used for assignments and used in the lecture notebooks
go here.  Some data files are local to the repository, but for larger data
files, scripts may be used to download a larger data file to this
repository data directory for local use.

**docs**/

Additional documentation for the class.  Class syllabus, and possible
assingment descriptions, slides and handouts will be placed here.

**figures**/

All static image files used in documents and notebooks. Images may
be generated by code and saved as part of a notebook or workflow, or
may be static images captured for use in documentation.

**lectures**/

Jupyter/iPython notebooks used for course lectures, video lectures and in
general the main resource with the course textbook and assignments for  
learning the course concepts.

**scripts**/

Separate executable scripts used to set up project aspects, load data for
the project, etc.  Bootstrap scripts are used by the Vagrant box
provisioning process to set up the virtual vagrant box for use by the
project.

**src**/

Project package(s) for this class.  Functions and classes that are of
general use in more than one notebook are pulled out as functions
(into the `custom_funcs.py` file), or separate functions and classes.
The `ml_python_class` module can be installed in the normal Python way on the system using
the `setup.py` file if needed, or it can be dynamically added to the
python path using for example:

```python
import sys
sys.path.append('../src')

from ml_python_class.custom_funcs import version_information
version_information()
```

**README.md, LICENSE**

Top level markdown files holding general project information.  
README.md markdown files may also be given in subdirectories for
further information about aspects of the project.

**Vagrantfile**

A standard vagrant init file.  Contains the configuration and
specifications to download and provision a vagrant box running
Anaconda Python3 and a JupyterHub/JupyterLab server.



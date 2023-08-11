![INSA](https://gi.insa-lyon.fr/sites/all/themes/insa_satellites/logo.png)

# GI-5-DSC - Data Science
***

This git repository contains the tutorial files for the [Data Science](https://moodle.insa-lyon.fr/course/view.php?id=4628) course of 5GI INSA Lyon.

This document explains how to install and set up a python environment with conda and install all the required libraries.

**Information** For those who have troubles installing a python environment on your computer you can simply download notebooks files (`.ipynb`) from this repository and run them remotely with [Google Colab](http://colab.research.google.com) (*Google account needed*).

***

## 1. Install conda

[Conda](https://conda.io/projects/conda/en/latest/index.html) is an open-source package management system and environment management system. It quiclky installs, runs and updates packages and their dependencies. 
We will use it for managing the python environment and all the python libraries needed for the tutorials.
There are several ways to install conda on your computer:
1. [Anaconda distribution](https://www.anaconda.com/products/distribution): provides GUI applications, a lot of data science and machine learning package already installed
2. [Miniconda](https://docs.conda.io/en/latest/miniconda.html): a minimal installer for conda, no GUI application
3. [Miniforge](https://github.com/conda-forge/miniforge): another minimal installer for conda, no GUI application (recommended for the Mac M1 or M2 chips (Apple Silicon))

## 2. Set up a conda environment

### 2.1 Download configuration files

#### 2.1.1 Method 1

* Clone this github repository

```bash
git clone https://github.com/ludovicmoncla/insa-5gi-dsc-tutorials.git
```

#### 2.1.2 Method 2

* Download and save the following files in one of your folder :
    - requirements.txt 


### 2.2 Configure the environment with all dependencies


* Create a new environment called `dsc-5gi-py39`

```bash
conda create -n dsc-5gi-py39 python=3.9
```

* Activate the environment

```bash
conda activate dsc-5gi-py39
```

* Install fiona package with `conda` (this prevent an issue while installing geopandas with `pip`)

```bash
conda install fiona=1.8.21
```

* Install dependencies with `pip`

```bash
pip install -r requirements.txt
```


### 2.3 Launch the jupyter server

```bash
jupyter notebook
```


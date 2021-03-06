# Deep Learning using TensorFlow at Datagiri

Code, Slides and other material for the talk on Deep Learning using TensorFlow at Datagiri meetup (Feb, 2017)

# How to Set Up

1. Install Anaconda
2. Install necessary packages

Notes
* In the following steps, we install a cpu-specific version of `tensorflow`, which is good enough for the session, but not for most real-world tasks.
* The instructions have been tested only on Ubuntu and OS X (we didn't have a windows system available for testing; please raise a issue if you hit any snags on your windows system).

---

## Install Anaconda

(Updated from [Udacity's instructions](https://github.com/soumendra/CarND-Term1-Starter-Kit/blob/master/doc/configure_via_anaconda.md))

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system 
for installing multiple versions of software packages and their dependencies and 
switching easily between them. It works on Linux, OS X and Windows, and was created 
for Python programs but can package and distribute any software.

### Overview

Using Anaconda consists of the following:

1. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer
2. Create a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html)
3. Each time you wish to work, activate your `conda` environment


### Installation

**Download** the version of `miniconda` that matches your system. Make sure you download the version for Python 3.x (3.6 is the latest at the time of writing).

|        | Linux | Mac | Windows | 
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install


---

## Install necessary packages

**Setup** your the `tensorflow` environment. 

```sh
git clone https://github.com/soumendra/lecture_datagiri_deeplearning_tensorflow_Feb17.git
cd lecture_datagiri_deeplearning_tensorflow_Feb17
```

If you are on Windows, **rename**   
`meta_windows_patch.yml` to   
`meta.yml`

**Create** `tensorflow`.  Running this command will create a new `conda` environment that is provisioned with all libraries you need to run the notebooks.
```
conda env create -f environment.yml
```

**Verify** that the `tensorflow` environment was created in your environments:

```sh
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```sh
conda clean -tp
```

### Uninstalling 

To uninstall the environment:

```sh
conda env remove -n tensorflow
```

---


## Using the Anaconda environment

Now that you have created an environment, in order to use it, you will need to activate the environment. This must be done **each** time you begin a new working session, i.e., open a new terminal window. 

**Activate** the `tensorflow` environment:

### OS X and Linux
```sh
$ source activate tensorflow
```

### Windows
Depending on shell either:
```sh
$ source activate tensorflow
```

or

```sh
$ activate tensorflow
```

That's it. Now all of the `tensorflow` libraries are available to you. You can start a Jupyter Notebook with:

```sh
jupyter notebook
```

To exit the environment when you have completed your work session, simply close the terminal window.


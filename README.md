# Setting up your computer for CMSC422

Welcome to CMSC422! Clone this repository and follow the instructions below to get set up!

In this class, we will use [Conda](https://conda.io) to manage Python and Python environments, and [Jupyter Notebooks](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb) to both implement and apply new machine learning algorithms.

## Setting up Python
As some of you might already know, Python 2.7 will be deprecated and will not be maintained past January 1, 2020. Hence, we will use Python 3.7 in this course.

We will also standardize our Python environments to better manage packages that we will all need for this course. The tool we will use to manage both Python itself, and Python pacakages will be [Conda](https://conda.io/docs/) (miniconda to be exact).

### Step 0: Install Conda
Conda is a utility that can manage both Python runtimes and Python Packages. We use Conda to ensure that the code we give you, and the code we receive from you are run on the same version of Python same version of different Python packages.

Follow this [guide](https://conda.io/docs/user-guide/install/index.html) and **install Conda on your machine**. (Note: once you select which OS you are using, please make sure to use the *miniconda installer* for your OS of choice.)

Once you have Conda installed **run `conda -V` in your command prompt** to ensure that you have Conda version 4.x.x.

### Step 1: Setup the CMSC422 Conda environment

We use Conda to manage the Python version and Python packages we need for a projects or, in our case, a particular set of assignments. Using Conda, we can isolate the Python and our desired packages in a *Conda environment* (think a virtual machine for just Python). By utilizing Conda environments, we standardize the python packages we all use which will in turn help us communicate and collaborate!

We can define the packages we need and the python version using YAML file. We have specified the Conda environment that you will need for this class. The file looks something like this...

```YAML
# Name the environment (CMSC422)
name: CMSC422

channels:
- conda-forge
- default

# Install the following dependencies!
dependencies:
- python=3.7
- numpy=1.*
- scikit-learn=0.*
- matplotlib=2.*
- jupyter=1.*
```

Now, **install the Conda environment with the above specifications and run the the following command** (this will take several minutes).
```
conda env create -f environment.yml
```

Now that you have the `CMSC422` Conda environment built, **activate it  by running**:

```
conda activate CMSC422
```
You should now see `(CMSC422)` on your command line indicating that you are using the `CMSC422` conda environment.

**Check the installed packages with**,
```
conda list
```
and **also run**,
```
python --version
```
to see that you do indeed have Python 3.7 running.

Now, **deactivate your environment** and return to your normal command prompt by running,
```
conda deactivate
```

### Step 2: Write/Run a Jupyter Notebook - Hello  world

Now you are ready to run your first Jupyter Notebook! First **activate** the `CMSC422` Conda environment and then **run the Jupyter Notebook server locally** with:
```
jupyter notebook .
```

and you should see a message like the following in your terminal.
```
[I 10:38:55.849 NotebookApp] Serving notebooks from local directory: /home/jason/dev/umd/CMSC422-Fall-2018-dev
[I 10:38:55.850 NotebookApp] The Jupyter Notebook is running at:
[I 10:38:55.850 NotebookApp] http://localhost:8888/\?token\=af9428c95a135a912aeb6e7afa16934b314dcfa5aee6ce94
[I 10:38:55.850 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 10:38:55.855 NotebookApp]

    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:8888/\?token\=af9428c95a135a912aeb6e7afa16934b314dcfa5aee6ce94
```

Now **open the your favorite browser** and **go to the given URL**. Click on `hello_world.ipynb` to get started with your first Jupyter Notebook.

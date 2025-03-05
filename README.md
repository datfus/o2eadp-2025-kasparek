# Experimental data analysis in plasma physics (02EADP)

## Install

To submit assignments, you need to first clone the repository and create a Python virtual environment to run your code.

### Clone the repository

You will be given access to your own repository named `o2eadp-2025-<YOURNAME>`. Clone it to your local machine:

```shell
cd /folder/where/you/want/to/clone/the/repository
git clone git@github.com:datfus/o2eadp-2025-<YOURNAME>.git
```

Create a folder for your assignments inside the repository, using your name:

```shell
mkdir assignments/<YOURNAME>
```

Put all your assignments in this folder. To avoid conflicts when the repository is updated, please do not modify any other files in the repository.

### Option 1: Create virtual environment using Poetry (Recommended)

The recommended way to create a virtual environment is using [Poetry](https://python-poetry.org/docs/#installation).

1. Install Poetry:
```shell
pipx install poetry
```

2. Install project dependencies:
```shell
cd o2eadp-2025-<YOURNAME>
poetry install
```

Your VS Code IDE should automatically detect the new virtual environment. Look for `o2eadp-2025-<YOURNAME>` in the list of Python kernels (you may need to restart VS Code).

To find the environment's location in your file system:
```shell
poetry env info
```

To add new packages to the environment:
```shell
poetry add <package>
```

When the repository is updated upstream (in the main branch), update your local repository and refresh the environment:
```shell
git checkout main
git pull
git checkout <your-working-branch>
git merge main
poetry install
```

This pulls the latest changes from main, merges them into your working branch, and updates your virtual environment with any new dependencies from `pyproject.toml`.

### Option 2: Create a separate virtual environment

Alternatively, you can create a separate virtual environment (using `conda` or `venv`) and install this package into it. This will automatically install all required dependencies. Here's how to do it with `venv`:

1. Create and activate the environment:
```shell
cd /folder/where/you/want/to/store/the/environment
python -m venv o2eadp-2025-<YOURNAME>
source o2eadp-2025-<YOURNAME>/bin/activate
```

2. Install the `o2eadp` package and its dependencies:
```shell
pip install git+ssh://github.com/datfus/o2eadp-2025-<YOURNAME>.git
```

When the package is updated upstream, update it in your environment:
```shell
pip install --upgrade git+ssh://github.com/datfus/o2eadp-2025-<YOURNAME>.git
```

## Example notebooks

The repository contains a few example notebooks that showcase the different methods and libraries discussed in the course and test the functionality of the environment.

### 01-fitting

[`examples/01-fitting/01-01-linear_regression.ipynb`](examples/01-fitting/01-01-linear_regression.ipynb) notebook shows how to do linear regression and uncertainty quantification with different methods and libraries. It's a long notebook primarily intended to test the functionality of the environment, but you can use it to get an overview and basic usage of the different methods and libraries.


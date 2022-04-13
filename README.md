# python_starter_project

Standard template for a python project with `tox` and GitHub workflows.

---

## Usage

Create project directory and pull the starter repo.

```text
$ mkdir myproject
$ cd myproject

# Pull python starter repo
$ git pull https://github.com/stanislavsabev/python_starter_proj.git
```

Setup virtual environment

```text
# Setup virtual environment and activate it
$ python -m venv venv
$ source ./venv/bin/activate # On Windows -> .\venv\Scripts\activate.bat
```

Install requirements

```text
$ pip install -r requirements.txt
```

```text
$ pip install -r requirements-dev.txt
```

**NOTE:** At this point you can choose different name for the `python_starter` package.

1. Rename `src/python_starter` directory.

2. Change all mentions of `python_starter` in pyproject.toml, setup.cfg, setup.py, tests/test_start.py and (optional) example.py.

Install 'python_starter' package in edit mode

```text
$ pip install -e .
```

### Run checks locally

```text
$ pytest
...
tests\test_start.py .
[100%]

----------- coverage: platform win32, python 3.9.2-final-0 -----------
Name                             Stmts   Miss  Cover
----------------------------------------------------
src\python_starter\__init__.py       0      0   100%
src\python_starter\start.py          2      0   100%
----------------------------------------------------
TOTAL                                2      0   100%


========================================================================= 1 passed in 0.11s ===
```

```text
$ mypy src
Success: no issues found in 6 source files

$ flake8 src tests
0
```

```text
$ tox -e py37,mypy,flake8 # Change 'py37' based on your python version.
...
______________________________________________________________________________ summary ___
  py37: commands succeeded
  mypy: commands succeeded
  flake8: commands succeeded
  congratulations :)
```

### Run checks using GitHub Actions workflows

Create GitHub repo and push your changes.
For more information see [GitHub Actions workflows](https://docs.github.com/en/actions/using-workflows) documentation.

![tests](https://github.com/stanislavsabev/python_starter_proj/actions/workflows/tests.yaml/badge.svg)

# Regresión con Python y scikit-learn

**Version**: 1.0
**Author**: pahoalapizco

Notes and exercises from courses linear regression and logistic regression with python and scikit-learn library.

## Prerequisites
- Anaconda >=4.x 

## Create environment
```bash
conda env create -f environment.yml
activate regresion_python
```

## Set up project's module
To move beyond notebook prototyping, all reusable code should go into the module/ folder package. To use that package inside your project, install the project's module in editable mode, so you can edit files in the final folder and use the modules inside your notebooks:

```bash
pip install --editable .
```

To use the module inside your notebooks, add `%autoreload` at the top of your notebook :

```python
%load_ext autoreload
%autoreload 2
```

Example of module usage :

```python
import sys
sys.path.append("..")

import modules.utils.paths as path
```

## Project organization

    regresion_python
        ├── data
        │   ├── processed      <- The final, canonical data sets for modeling.
        │   └── raw            <- The original, immutable data dump.
        │
        ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
        │                         the creator's initials, and a short `-` delimited description, e.g.
        │                         `1.0-initial-data-exploration`.
        │
        ├── .gitignore         <- Files to ignore by `git`.
        │
        ├── environment.yml    <- The requirements file for reproducing the analysis environment.
        │
        ├── README.md          <- The top-level README for developers using this project.
        │
        ├── setup.py           <- Makes project pip installable (pip install -e .)
        │                          so final can be imported.
        ├── .here              <- File that will stop the search if none of the other criteria
        │                         apply when searching head of project.
        │
        └── module              <- Source code for use in this project.
            └── utils          <- Scripts to help with common tasks.
                └── paths.py   <- Helper functions to relative file referencing across project.

---
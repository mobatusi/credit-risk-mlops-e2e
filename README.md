# E2E ML project using open-source MLOps tools

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

## Project Description
This project is an extension of the Datacamp Credit Risk Modeling in Python Course, leveraging an end-to-end (E2E) machine learning project using open-source MLOps tools. The aim is to build and deploy a robust credit risk model.

## Problem Description and Dataset
The dataset consists of 32,000 rows, each representing a unique bank customer. It includes two primary types of data crucial for modeling the probability of default:

1. **Application Data**: Information directly tied to the loan application, such as loan grade.
2. **Behavioral Data**: Information about the loan recipient, such as employment length.

The combination of application and behavioral data enhances predictive accuracy compared to using application data alone. Additionally, the dataset includes two columns that simulate data obtainable from credit bureaus, reflecting common practices in many organizations. Examples of the data available in the dataset include personal income, the loan amount as a percentage of the person's income, and credit history length. These factors can influence loan status; for instance, if the loan amount exceeds the individual's income, they might struggle to afford payments.

Dataset source: [Datacamp Credit Risk Modeling in Python Course](https://assets.datacamp.com/production/repositories/4876/datasets/a2d8510b4aec8d0ac14ab9bee61ba3c085805967/cr_loan2.csv)

## Use Case
The objective is to train an ML model that returns the probability of default. We will use the XGBoost package in Python to create gradient boosted trees. We will also use logistic regression, a standard for risk modeling. After developing and testing these two powerful machine learning models, we use key performance metrics to compare them. Using advanced model selection techniques specifically for financial modeling, we will select one model. With that model, we will: develop a business strategy, estimate portfolio value, and minimize expected loss.

## Setup
Python 3.8+ is required to run code from this repo.
```
$ git clone https://github.com/mobatusi/credit-risk-mlops-e2e
$ cd credit-risk-mlops-e2e
$ virtualenv -p python3 .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
```
## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for credit_risk_mlops_e2e
│                         and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── credit_risk_mlops_e2e                <- Source code for use in this project.
    │
    ├── __init__.py    <- Makes credit_risk_mlops_e2e a Python module
    │
    ├── data           <- Scripts to download or generate data
    │   └── make_dataset.py
    │
    ├── features       <- Scripts to turn raw data into features for modeling
    │   └── build_features.py
    │
    ├── models         <- Scripts to train models and then use trained models to make
    │   │                 predictions
    │   ├── predict_model.py
    │   └── train_model.py
    │
    └── visualization  <- Scripts to create exploratory and results oriented visualizations
        └── visualize.py
```

--------


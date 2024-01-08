# Model-Packaging

## Overview

This lab focuses on designing a package that transitions from a research environment to a production environment. Unlike research code, which is aimed at conducting local experiments or proofs-of-concept, production code must be robust, scalable, and user-friendly.

## Objectives

- **Testability & Maintainability**: Modularize code for easy testing and extension.
- **Configuration Separation**: Keep configuration separate from code, ensuring thorough testing and documentation of each feature.
- **Code Standards**: Adhere to standards like PEP-8 for readability.
  - [PEP-8 Guide](https://www.python.org/dev/peps/pep-0008/)
- **Scalability & Performance**: Ensure deployment in scalable infrastructures.
- **Reproduction & Monitoring**: Use version control and dependency files for consistent code reproduction.
- **Publication**: The package will be published on PyPI for installation via `pip`.

## Tutorial Reference

Follow the official tutorial for packaging projects:  
[Python Packaging User Guide](https://packaging.python.org/tutorials/packaging-projects/)

### Overview of Our Package

We explore the transition from a research environment to a production package.

#### Requirements Folder

- Contains `requirements.txt` and `test_requirements.txt`.
- Install requirements: `pip install -r requirements/requirements.txt`.
- Includes dependencies like Black, Flake8, Mypy, Isort.

#### Management and Testing using Tox

- Tox is used for managing and testing the package.
- Configuration details in `tox.ini`.
- Commands: `tox –e lint`, `tox –e train`, etc.

#### Package Configuration

- Configuration file: `config.yml`.
- Use of YAML for broader accessibility.
- Python classes in `core.py` for managing configurations.

#### Model Training and Pipeline Execution

- `train_pipeline.py` for model training.
- Use of `config` object from `core.py` for managing data and metadata.

#### Features Engineering

- `pipeline.py` and `features.py` for feature transformations.
- Testing with `test_features.py` and `conftest.py`.

#### Prediction

- `predict.py` for making predictions.
- Testing predictions in `test_prediction.py`.

#### Package Construction

- Packaging files: `pyproject.toml`, `setup.py`, `MANIFEST.in`.
- Steps for building and publishing the package as per the Python Packaging User Guide.

## Conclusion

This lab guides you through the entire process of converting a research-oriented codebase into a production-ready package, emphasizing best practices in software development, packaging, and deployment.

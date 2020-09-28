# Python Project Template Cookiecutter

This cookiecutter template provides a default template for a standard Python project, just Python, nothing else. Anything else required would need to be installed after creating project from this cookiecutter.

Best practices [cookiecutter](https://github.com/audreyr/cookiecutter) template as described in this [blogpost](https://sourcery.ai/blog/python-best-practices/).

This uses pre-commit command too, check it [here](https://pre-commit.com/). 

Also, there are a couple of Github workflow actions, one to Publish the Docker image (based on [this](https://github.com/whoan/docker-build-with-cache-action)) to the registry and also another one that runs test on Docker image too. More info on Github actions [here](https://docs.github.com/en/free-pro-team@latest/actions/learn-github-actions/finding-and-customizing-actions)

## Features
- Testing with [pytest](https://docs.pytest.org/en/latest/)
- Formatting with [black](https://github.com/psf/black)
- Import sorting with [isort](https://github.com/timothycrosley/isort)
- Static typing with [mypy](http://mypy-lang.org/)
- Linting with [flake8](http://flake8.pycqa.org/en/latest/)
- Git hooks that run all the above with [pre-commit](https://pre-commit.com/)
- Deployment ready with [Docker](https://docker.com/)
- Continuous Integration with [GitHub Actions](https://github.com/features/actions)

## Quickstart
```sh
# Install pipx if pipenv and cookiecutter are not installed
python3 -m pip install pipx
python3 -m pipx ensurepath

# Install pipenv and pre-commit using pipx
pipx install pipenv
pipx install pre-commit

# Use cookiecutter to create project from this template
pipx run cookiecutter gh:internetmosquito/python-project-template-cookiecutter

# Enter project directory
cd <repo_name>

# Initialise git repo
git init

# Create virtualenv with pipenv, choose whatever Python version as long as it matches the one in Pipfile, OR you can skip this altogether if your default version 
# is the same as the one in Pipfile 
pipenv --python 3.7 

# Install dependencies
pipenv install --dev

# Setup pre-commit and pre-push hooks
pipenv run pre-commit install -t pre-commit
pipenv run pre-commit install -t pre-push
```

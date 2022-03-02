# Project Setup

[![Production Workflow](https://github.com/arunkatta97/docker-flask/actions/workflows/prod.yml/badge.svg)](https://github.com/arunkatta97/docker-flask/actions/workflows/prod.yml)

* [Production Deployment](https://ak-flask-prod.herokuapp.com/)


[![Development Workflow](https://github.com/arunkatta97/docker-flask/actions/workflows/dev.yml/badge.svg)](https://github.com/arunkatta97/docker-flask/actions/workflows/dev.yml)

* [Developmental Deployment](https://ak-flask-prod.herokuapp.com/)

## Setting up CI/CD

#### Setup Docker and Heroku Credentials In the Repository Settings under Action -> Secret

6. In your newly created Github repository, add new repository secrets for DOCKER_USERNAME, DOCKER_PASSWORD, HEROKU_API_KEY (Values are DOCKER_USERNAME: your docker hub username; DOCKER_PASSWORD: your docker hub password; HEROKU_API_KEY: API key from the heroku app)
### GitHub Notes:  Set the action secrets repository in: -> settings -> actions -> secrets
### Heroku Notes: Get the heroku API key from account in: -> applications -> create authorization button

#### Change GitHub Actions Workflows for Dev and Prod

6. Change line 42 to have your docker repo address in: .github/workflows/prod.yml
7. change lines 58 to have your heroku app name in: .github/workflows/prod.yml
8. change line 59 to have your heroku email in: .github/workflows/prod.yml
9. change line 31 to have your heroku app name in .github/workflows/dev.yml
10. change line 32 to have your heroku email in .github/workflows/dev.yml
11. Push code to your local repo and check for any errors and fix any errors that appear when the workflow is running. You can check the workflow in the
    actions.

## Running Locally

1. To Build with docker compose:
   docker compose up --build
2. To run tests, Lint, and Coverage report use this command: pytest --pylint --cov

.pylintrc is the config for pylint, .coveragerc is the config for coverage and setup.py is a config file for pytest


### Future Notes and Resources
* https://flask-user.readthedocs.io/en/latest/basic_app.html
* https://hackersandslackers.com/flask-application-factory/
* https://suryasankar.medium.com/a-basic-app-factory-pattern-for-production-ready-websites-using-flask-and-sqlalchemy-dbb891cdf69f

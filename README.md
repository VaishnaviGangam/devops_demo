# DevOps Demo

A Python application repository with a Docker-based delivery workflow and GitHub Actions automation.

## CI/CD workflow

The workflow in `.github/workflows/production.yml` runs on pushes and pull requests targeting `main`.

1. Checks out the repository.
2. Sets up Python 3.9.
3. Installs dependencies.
4. Runs the test suite with Pytest.
5. Builds a Docker image and pushes it to Docker Hub after the test job succeeds.

## Technology

Python · Pytest · Docker · GitHub Actions · Docker Hub

## Repository contents

- `.github/workflows/production.yml` — CI/CD pipeline
- `Dockerfile` — container build configuration
- `requirements.txt` — Python dependencies

## Required repository secrets

Configure the following GitHub Actions secrets before enabling the image-publishing step:

- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN`

The workflow publishes the image as `vg523/devops_demo:latest`.
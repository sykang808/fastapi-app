# FastAPI Sample Application

A sample FastAPI application that demonstrates how to use common GitHub Actions workflows.

## Features

- Simple FastAPI application with sample endpoints
- Integrated CI/CD pipeline using reusable GitHub Actions workflows
- Containerized using Docker

## Running Locally

1. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

2. Run the application:

   ```
   uvicorn app.main:app --reload
   ```

3. Access the API documentation:
   Open your browser and navigate to `http://localhost:8000/docs`

## CI/CD Pipeline

This project uses reusable GitHub Actions workflows from the [github-actions-common](https://github.com/your-org/github-actions-common) repository:

1. **Test**: Runs Python tests on every push and PR
2. **Build**: Builds a Docker image when merged to main
3. **Deploy**: Deploys to the development environment when merged to main

## Required Secrets

To use the CI/CD pipeline, the following secrets must be configured in your GitHub repository:

- `REGISTRY_USERNAME`: Username for container registry
- `REGISTRY_PASSWORD`: Password for container registry
- `REGISTRY_URL`: URL of container registry (optional)
- `DEV_SSH_HOST`: SSH host for development environment
- `DEV_SSH_USERNAME`: SSH username for development environment
- `DEV_SSH_KEY`: SSH private key for development environment

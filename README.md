# CI/CD Pipeline Automation using Jenkins, Docker & AWS EKS

## Overview

This project demonstrates an end-to-end CI/CD pipeline using Jenkins Declarative Pipeline. The pipeline automates source code checkout, application build, Docker image creation, image publishing to Docker Hub, and deployment to an Amazon EKS Kubernetes cluster.

## Tech Stack

- Jenkins
- Git & GitHub
- Maven
- Docker
- Docker Hub
- AWS CLI
- Amazon EKS
- Kubernetes (kubectl)
- Linux

## Pipeline Workflow

```
GitHub
   │
   ▼
Jenkins
   │
   ▼
Maven Build
   │
   ▼
Docker Build
   │
   ▼
Docker Hub
   │
   ▼
AWS EKS
   │
   ▼
Kubernetes Deployment
```

## Pipeline Stages

### 1. Checkout Code
- Fetches source code from GitHub.

### 2. Maven Build
- Builds the application using Maven.

### 3. Docker Build
- Creates a Docker image tagged with the Jenkins build number.

### 4. Docker Hub Push
- Authenticates with Docker Hub using Jenkins credentials.
- Pushes the Docker image to Docker Hub.

### 5. Kubernetes Deployment
- Updates the kubeconfig for the Amazon EKS cluster.
- Deploys the application using Kubernetes manifests.

## Prerequisites

- Jenkins
- Java
- Maven
- Docker
- AWS CLI
- kubectl
- Docker Hub Account
- Amazon EKS Cluster
- Jenkins Credentials

## Jenkins Credentials

| Credential ID | Purpose |
|---------------|---------|
| aws-cred | AWS Authentication |
| docker-cred | Docker Hub Authentication |

## Repository Structure

```
Project-Docker-on-Jenkins/
│
├── Jenkinsfile
├── Dockerfile
├── Application.yaml
├── pom.xml
└── src/
```

## Running the Pipeline

1. Configure Maven in Jenkins.
2. Add `aws-cred` and `docker-cred` in Jenkins Credentials.
3. Install Docker, AWS CLI, and kubectl on the Jenkins server.
4. Create an Amazon EKS cluster.
5. Commit the code to GitHub.
6. Trigger the Jenkins pipeline.

## Features

- Automated CI/CD pipeline
- Docker image creation
- Docker Hub integration
- Amazon EKS deployment
- Secure credential management
- Kubernetes deployment automation

## Future Enhancements

- Add SonarQube for code quality analysis
- Integrate Trivy for Docker image scanning
- Add automated unit testing
- Configure Slack/Email notifications
- Implement blue-green or rolling deployments

## Author

**Muskan Baboo**

# CI/CD Practice Project with Tekton and Kubernetes

This repository is a complete CI/CD practice project that demonstrates modern DevOps workflows using Tekton Pipelines, Kubernetes, Docker, and GitHub Actions. It includes automation for testing, building, and deploying a Flask application in a containerized environment.

# Project Structure
```
├── .devcontainer/ # VS Code development container config
├── .github/ # GitHub Actions & issue templates
├── bin/ # Utility scripts
├── deploy/ # Kubernetes manifests
├── service/ # Flask application source code
├── tekton/ # Tekton pipeline, tasks, and PVC definitions
├── tests/ # Unit tests
├── Dockerfile # Container image definition
├── Makefile # CLI shortcuts for development
├── requirements.txt # Python dependencies
├── setup.cfg # Python test config
├── postgresql-ephemeral-template.json # Ephemeral DB template
├── Procfile # Heroku deployment
├── LICENSE # Apache 2.0 License
└── README.md # You're here!
```

# Technology Stack

- Flask (Python)
- Docker
- Tekton Pipelines
- Kubernetes
- GitHub Actions
- Python unittest

# Learning Objectives

- Design and implement Tekton CI/CD pipelines
- Automate testing and image builds
- Use Kubernetes for automated deployment
- Apply GitOps and Infrastructure as Code
- Improve container security and observability

# Lab Progression

## Lab 01: Base Pipeline
- Basic Tekton pipeline structure and execution

## Lab 02: Git Trigger
- Add webhook-based Git triggers

## Lab 03: Tekton Catalog
- Use reusable tasks from the Tekton Catalog
- Add PVC for storage

## Lab 04: Unit Testing
- Integrate test automation
- Add quality gates and failure handling

## Lab 05: Build Image
- Build Docker images within pipeline
- Add security scanning and tagging

## Lab 06: Kubernetes Deployment
- Automate deployment with rolling updates
- Add service mesh and observability

# Getting Started

## Prerequisites

- Python 3.8 or higher
- Docker
- Kubernetes cluster access
- Tekton Pipelines installed

## Local Development

```
git clone https://github.com/ongunakaycom/ibm-developer-skills-network-wtecc-CICD_Practice
cd ibm-developer-skills-network-wtecc-CICD_Practice
pip install -r requirements.txt
flask run
```

## Docker Development

```
docker build -t cicd-practice .
docker run -p 5000:5000 cicd-practice
```

# Tekton Pipeline Execution

1. Apply pipeline definitions:

kubectl apply -f tekton/

2. Configure secrets, service accounts, and PVCs
3. Trigger the pipeline manually or via webhook
4. Monitor using Tekton Dashboard

# Testing

python -m unittest discover tests/

Test files include:

- tests/test_routes.py
- tests/test_models.py
- tests/test_error_handlers.py
- tests/test_cli_commands.py

Tests are automatically executed in CI/CD pipelines.

# Configuration Highlights

- Dockerfile: Multi-stage image build
- .flaskenv: Environment variables for Flask
- setup.cfg: Test config
- .github/workflows/ci-build.yaml: GitHub Actions CI pipeline
- tekton/: All Tekton task, pipeline, and PVC definitions

# Contribution Guide

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add or update tests
5. Submit a pull request

## 🤝 Contributing

Pull requests and feedback are welcome! If you'd like to contribute improvements, feel free to fork and submit a PR.

---

## About Me

I'm Ongun Akay, a Senior Full-Stack Developer with expertise across various technologies.

- 👀 I specialize in full-stack development with extensive experience in frontend and backend technologies.
- 🌱 Currently, I'm sharpening my skills in advanced concepts of web development.
- 💞️ I’m always open to exciting collaborations and projects that challenge my abilities.
- 📫 You can reach me at [info@ongunakay.com](mailto:info@ongunakay.com).

---

## 📄 License

This project is licensed under the [Apache-2.0 license](./LICENSE) — see the LICENSE file for details.

Refer to each lab's README or the IBM Developer Skills Network for detailed lab instructions and setup documentation.
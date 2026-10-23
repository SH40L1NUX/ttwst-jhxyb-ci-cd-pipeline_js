##JavaScript CI/CD implementation, documenting GitHub Actions, Tekton, OpenShift, testing, and deployment.

# JavaScript CI/CD Final Project — OpenShift Pipeline

## Project Overview

This repository contains the JavaScript implementation of the final project for the **Continuous Integration and Continuous Delivery (CI/CD)** course on Coursera.

The project demonstrates how to automate application validation, testing, container image building, and deployment using GitHub Actions, Tekton, and Red Hat OpenShift.

The objective is to establish a repeatable CI/CD workflow that validates application changes and supports deployment through an OpenShift pipeline.

## Technologies Used

- **JavaScript** — application and automated testing implementation.
- **GitHub** — source control and project versioning.
- **GitHub Actions** — automated workflow execution and code validation.
- **ESLint** — JavaScript code linting.
- **Jest** — automated unit testing.
- **Tekton** — Kubernetes-native CI/CD tasks and pipeline automation.
- **Red Hat OpenShift** — container application deployment and pipeline execution.
- **Buildah** — container image building.
- **PersistentVolumeClaim (PVC)** — persistent storage provisioning for the OpenShift environment.

## Project Objectives

The project implements the following CI/CD capabilities:

1. Maintain the application source code in a GitHub repository.
2. Automate JavaScript linting and unit tests using GitHub Actions.
3. Define reusable Tekton tasks for pipeline operations, including cleanup and automated testing.
4. Configure and execute a CI/CD pipeline in OpenShift.
5. Build and deploy the application using the configured pipeline.
6. Verify successful workflow execution and inspect application logs.
7. Capture the required evidence to demonstrate the completed implementation.

## Continuous Integration — GitHub Actions

The GitHub Actions workflow is defined in:

`.github/workflows/workflow.yml`

The workflow automates the validation process, including:

- Checking out the repository source code.
- Preparing the required JavaScript runtime and dependencies.
- Running ESLint to identify code-quality and linting issues.
- Running Jest unit tests to validate application behaviour.
- Reporting the workflow execution status through the GitHub Actions interface.

These automated checks provide feedback on code changes before the application proceeds through the deployment workflow.

## Tekton Tasks

The Tekton task definitions are located in:

`.tekton/tasks.yml`

The configuration includes the cleanup task and the JavaScript testing task required by the course project.

The Jest testing task supports automated execution of the application's unit tests within the Tekton environment. The cleanup task provides a defined mechanism for the relevant pipeline cleanup operations.

## Continuous Delivery — OpenShift

Red Hat OpenShift provides the environment for executing the CI/CD pipeline and deploying the application.

The pipeline integrates the configured tasks to support the application delivery process, including the relevant build, validation, and deployment operations.

Buildah is used for container image building as configured in the project environment.

The OpenShift implementation also includes persistent storage configuration through a PersistentVolumeClaim (PVC).

Pipeline execution and application status can be inspected through the OpenShift console and the available application logs.

## Validation and Verification

The implementation is verified using the following evidence:

- GitHub Actions workflow execution results.
- ESLint and Jest workflow steps.
- Tekton cleanup and Jest task definitions.
- OpenShift PersistentVolumeClaim details.
- OpenShift pipeline configuration.
- Successful OpenShift pipeline execution.
- Application logs from the OpenShift environment.

The evidence files are prepared separately in accordance with the Coursera final project submission criteria.

## Repository Structure

The following paths contain the key CI/CD configuration files:

```text
.
├── .github/
│   └── workflows/
│       └── workflow.yml
├── .tekton/
│   └── tasks.yml
└── README.md
```

The application source code, tests, and any additional configuration files are maintained in their respective repository locations.

## Learning Outcomes

This project demonstrates practical experience with:

- Implementing automated CI validation using GitHub Actions.
- Applying JavaScript linting and unit testing.
- Defining CI/CD tasks using Tekton.
- Working with container image builds using Buildah.
- Configuring pipeline execution and application deployment on OpenShift.
- Verifying pipeline outcomes and troubleshooting deployment issues.
- Documenting technical implementation and collecting reproducible validation evidence.

## Course Context

**Course:** Continuous Integration and Continuous Delivery (CI/CD)  
**Project:** Final CI/CD Pipeline Project  
**Implementation:** JavaScript  
**Repository:** [ttwst-jhxyb-ci-cd-pipeline_js](https://github.com/SH40L1NUX/ttwst-jhxyb-ci-cd-pipeline_js)

---

This repository serves as a practical demonstration of integrating source control, automated code validation, container build tooling, Kubernetes-native pipeline tasks, and application deployment within a CI/CD workflow.

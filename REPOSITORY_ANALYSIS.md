# myYAML Repository Analysis

## Overview

The **myYAML** repository is a comprehensive starter project designed for learning and demonstrating YAML-based CI/CD pipelines, specifically Azure DevOps Pipelines. This repository serves as a tutorial project that showcases various .NET application types and their deployment strategies to Azure cloud services.

## Repository Structure

### Core Applications

The repository contains **four main application projects**:

#### 1. **oldDadApp** - Legacy ASP.NET MVC Application
- **Technology**: Traditional ASP.NET Framework 4.7.2 with MVC 5
- **Type**: Classic .NET Framework web application
- **Purpose**: Demonstrates legacy application deployment patterns
- **Key Features**:
  - Bootstrap-based responsive UI
  - MVC pattern implementation
  - Uses traditional Web.config configuration
  - Displays environment information (build number, machine name, OS, framework)
  - Branded as "Ask Dad..." application

#### 2. **myNewDadApp** - Modern ASP.NET Core Application  
- **Technology**: .NET Core 3.1 web application
- **Type**: Modern cross-platform web app
- **Purpose**: Shows modern .NET Core deployment with containerization
- **Key Features**:
  - Docker support with multi-stage Dockerfile
  - Modern ASP.NET Core structure
  - appsettings.json configuration
  - Cross-platform compatibility

#### 3. **myAPI** - Web API Service
- **Technology**: .NET Core 3.1 Web API
- **Type**: RESTful API service
- **Purpose**: Demonstrates microservice/API deployment patterns
- **Features**:
  - Weather forecast sample API
  - Swagger/OpenAPI integration
  - Docker container support
  - Independent deployment pipeline

#### 4. **myWebDeploy** - Infrastructure Templates
- **Technology**: Azure Resource Manager (ARM) templates
- **Type**: Infrastructure as Code (IaC) project
- **Purpose**: Defines Azure resources for application hosting
- **Components**:
  - Windows Web App with deployment slots
  - Linux Web App with deployment slots  
  - PowerShell deployment scripts
  - Parameter files for environment configuration

### CI/CD Pipeline Infrastructure

The repository contains **extensive Azure DevOps pipeline definitions**:

#### Main Pipeline Files
- **azure-pipelines.yml** - Primary production pipeline
- **azure-pipelines-1.yml** - Alternative pipeline configuration
- Multiple versioned pipelines (01-04, 01-06, 01-08, 02-02, etc.) - Tutorial progression

#### Pipeline Features
- **Multi-stage deployments** (Build → Test → Deploy)
- **Token replacement** for environment-specific values
- **Artifact management** and publishing
- **Azure Resource Group deployment**
- **Web application deployment** to Azure App Service
- **Build and test automation**

### Additional Components

#### Pattern Files
- **patterns-app-inflation.yml** - Application scaling patterns
- **patterns-docfx.yml** - Documentation generation patterns  
- **patterns-script-demo.yml** - Script execution patterns

#### Kubernetes Support
- **manifests/deployment.yml** - Kubernetes deployment configuration
- **manifests/service.yml** - Kubernetes service definition

#### Configuration Files
- **.gitignore** - Comprehensive ignore rules for .NET projects
- **.dockerignore** - Docker build exclusions
- **myYAML.sln** - Visual Studio solution file containing all projects

## Learning Objectives

This repository teaches:

1. **Pipeline Evolution** - Progressive pipeline complexity through numbered versions
2. **Multi-target Deployment** - Both Windows and Linux hosting scenarios  
3. **Technology Migration** - Legacy .NET Framework to modern .NET Core
4. **Container Strategies** - Docker integration and Kubernetes deployment
5. **Infrastructure as Code** - ARM template usage for Azure resources
6. **DevOps Best Practices** - Multi-stage pipelines, artifact management, environment promotion

## Architecture Patterns Demonstrated

### Deployment Slots Pattern
- **TEST** and **STAGING** slots for safe deployments
- Blue-green deployment capabilities
- Zero-downtime deployment strategies

### Multi-Stage Pipeline Pattern
- **BuildIt Stage** - Code compilation and testing
- **TestDeployment Stage** - Infrastructure provisioning and application deployment
- Artifact-based promotion between stages

### Containerization Pattern
- Multi-stage Docker builds for .NET Core applications
- Container registry integration
- Kubernetes orchestration support

## Technical Stack

### Frameworks & Runtime
- .NET Framework 4.7.2 (legacy app)
- .NET Core 3.1 (modern apps)
- ASP.NET MVC 5 (legacy)
- ASP.NET Core (modern)

### Cloud & DevOps
- Azure DevOps Pipelines
- Azure App Service (Windows & Linux)
- Azure Resource Manager
- Docker containerization
- Kubernetes orchestration

### Frontend Technologies
- Bootstrap CSS framework
- jQuery JavaScript library
- Responsive web design principles

## Repository Purpose

This repository serves as a **comprehensive educational resource** for:
- DevOps engineers learning Azure Pipelines
- Developers transitioning from legacy to modern .NET
- Teams implementing CI/CD best practices
- Organizations adopting Infrastructure as Code

The progressive pipeline files (numbered sequences) suggest this is used in a **structured learning curriculum**, allowing students to build knowledge incrementally from simple builds to complex multi-stage deployments.
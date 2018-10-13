# Azure Kubernetes Service (AKS) Learning Series

Demo code for Hands on Series for `Azure kubernetes Series (AKS) learning series`. 

## Code organization

- `Docker-compose V1`

Contains the docker-compose file in its simplest form

- `Docker-compose V2`

Contains the docker-compose files split into a base compose file and separate files for build and run scenarios. This is a preferred approach as it allows to have clear separation in terms of images which are built as part of application code and images which are used from other pre-built images. This also allows us to separate configurations between different environments like Dev / Integration / Production etc.

- `Helm`
Contains the Helm charts which are useful for deploying Kubernetes applications. Refer to the [Helm readme](/helm/Readme.md) file for more details.

- `k8s`

Contains Kubernetes Manifest files. These are grouped into `Minikube` version with services exposed using `NodePort` type. `AKS` version exposes the `TechTalksWeb` and `TechTalksDB` using LoadBalancer. The data is also persisted to outside of the container using `Persistent Volume (PV)` and `Persistent Volume Claim (PVC)`. The volume is backed by `Azure Disk`. 

- `Powershell`

Contains the powershell scripts used for deploying application resources to Minikube or AKS cluster

- `Skaffold`

[Skaffold](https://github.com/GoogleContainerTools/skaffold) adds ability to do continuous deployment of Kubernetes application. This is similar to live unit testing feature. Refer to the two links below to know more about using Skaffold.

1 - Use [Skaffold with Minikube](https://www.handsonarchitect.com/2018/08/continuous-kubernetes-deployments-with.html)

2 - Use [Skaffold with Docker for Mac with Kubernetes](https://www.handsonarchitect.com/2018/08/continuous-kubernetes-deployments-with.html)

- `src`

Contains the source code.
    
    - `TechTalksAPI` contains code for Web API project

    - `TechTalksDB` contains database initialization script

    - `TechTalksWeb` contains code for ASP.Net Core MVC frontend

- `Minikube`

Contains instructions for setting up `Minikube` cluster and `Kubectl`

## Setup Development environment

The project is based on .Net Core 2.1 framework. The application is built using Docker Multi-Stage builds and does not require the base machine to have .Net Core or runtime to be installed. It is recommended to install .Net Core framework locally on the machine if you wish to debug the code.

### Mac and CLI resources

This project was initially started with Mac and cross platform resources for .Net Core development including
- Visual Studio Code
- iTerm 2
- Powershell
- Docker for Mac

### Windows 10 and CLI resources

The application can be tested on Windows 10 using tools listed below
- Visual Studio Code
- Powershell
- Docker for Windows

### Windows 10 and Visual Studio 2017

For some people it is unimaginable to work our of Visual Studio.You can replace Visual Studio Code with Visual Studio 2017 as the preferred IDE. 



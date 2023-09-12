# Microservices

This documentation explains how we're envisioning our microservices archtecture

![alt text](/docs/images/Microservices.jpg)


## Tools  
- Backstage
   - TechDocs
   - Software Catalog
   - Software Templates
- Git
  - Github
  - Github Actions
  - Github Container Registry
- Docker
- FluxCD
- Kubernetes

## Backstage

Backstage is a tool that is used to host all things related to technical documentation and it also has some other cool features like being able to create a new repository based on a template.  
We're gonna create our repositories with that new feature.  
You can read more about what backstage can do here: [What is backstage?](https://backstage.io/docs/overview/what-is-backstage)

### TechDocs

TechDocs is a built-in plugin that comes with Backstage.  
It uses markdown files to produce rich technical documentation, and these files are stored close to the code.
This article that you're reading is a TechDoc, and you can learn more about TechDocs here: [TechDocs documentation](https://backstage.io/docs/features/techdocs/)

### Software Catalog

Software catalog is another built-in plugin that comes with backstage.  
It's used to track information about every service that we have in our ecosystem and it uses YAML files stored close to the code to display the information inside Backstage.  
You can read more here: [Software Catalog documentation](https://backstage.io/docs/features/software-catalog/)

### Software Templates

The last built-in plugin from Backstage that we're gonna use is Software Templates. It'll help us create new microservices based on our need.  
Whe we create a new microservice using Software Template, it'll automatically be registered in our Software Catalog, along with having a dedicated TechDoc with it.  
You can read more here: [Software Templates documentation](https://backstage.io/docs/features/software-templates/)


## Git

Git is no news for most dev teams, so if you wanna read more, you can read here: [Git Documentation](https://git-scm.com/doc)

### Github

We recently decided to move from Gitlab to Github. When it comes to our day to day work, it doesn't change much as it's still a git tool.  
Github is widely known and has a lot of features that are gonna be good for us, like Github Copilot, Gihub Actions, Github Container Registry.  

### Github Actions

Github Actions is a great tool that is gonna help us with our CI&CD process. The idea is to move away from Jekins and have our pipelines running on Github Actions.  
By default, all our newly created microservices are gonna build, pus a docker image and deploy to Kubernetes using Github Actions.  
It works as having the workflow files, that are YAML files, inside a `.github/workflows` directory at the root path of our repository.  
Our workflows are still in an early stage and we're learning as we go. You can read a lot more here: [Github Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)  

### Github Container Registry

Github Container Registry will be used to store all our docker images used to deploy the service to Kubernetes.


## Docker

## FluxCD

## Kubernetes

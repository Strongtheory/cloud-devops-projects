Note: This is very similar to the aws project however all resources with the exception of the terraform state files and docker images
      are provisioned on Azure.

Technologies:
* Azure
* Terraform: This is IaaC to spawn the reources on Azure.
* NestJS: REST API framework similar to express in nodejs.
* CircleCI: Devops tool to handle Continuous integration and development.
* AKS: AKS Kubernetes Cluster to manage the microservices and the pods.
* Docker: Images for each microservice.
* Traefik: I used Traefik as a loadbalancer with let's encrypt to reroute http traffic to https
  and distribute https requests evenly in the cluster. Also autoscale the pods if there is too much traffic.
* MySQL: DB server

* Description: Illustrates a sample of my work on deploying a microservices architecture for a react web app
  on aws with full CI/CD integration.

* Folders:
- Base: This contains the docker image used for the deployment folder which is stored in AWS ECR.
- Deployment: This folder contains the file to deploy and update all the resources used on AWS through terraform.
- authentication-microservice: This folder contains a NestJS project to handle basic authentication.
- user-microservice: This folder contains a NestJS project to handle basic user profile information.
- Advanced: I've added a few additional microservices such as messaging through web sockets and also file storage.

# Quick Lookup and Context Suite Deployment

This repo contains configuration for the our clusters and services.
We use Fleet (Rancher) to manage our Kubernetes clusters and Helm to deploy our services.

The Fleet service monitors this repo and deploys all services and applications that are mapped in Ranchder.

## Systems involved and their roles
The following systems are involved in deploying Quick Lookup and Context Suite services.

### Github
This repository is stored on Github and contains all configuration for the services and applications.
Whe it changes, Fleet will automatically deploy the changes to the cluster.

Our code is also stored in Github and is automatically build and dockerized by Github Actions.
Docker images are then stored in [DockerHub](#docker-hub).

### Rancher
Wee use Rancher to manage our all of our Kubernetes clusters, independent of the cloud provider.
Fleet is the part of Rancher that is used to monitor and deploy the configuration in this repo.

Our rancher instance is available at [ops.quicklookup.com](https://ops.quicklookup.com)</br>
[Rancher Docs](https://ranchermanager.docs.rancher.com/)</br>
[Fleet Docs](https://fleet.rancher.io/)

### Docker Hub
Whe store container images in DockerHub.
Fleet fetches the images from DockerHub and deploys them to the cluster based on the tags specified in this repo.
We can have Github Actions updated these tags automatically when code is pushed to Github.

[Our DocerHub Repo](https://hub.docker.com/repository/docker/quicklookup/)

## Solutions and Services supported by this repo

### Context Suite






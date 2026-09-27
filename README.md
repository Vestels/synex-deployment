# Synex Deployment

Deployment and infrastructure configuration for the Synex application.

## Local Development

Make sure all service repositories are placed within the same parent folder without changing their names.

Example:

    projects/
    ├── synex-deployment/
    ├── synex-eureka-server/
    ├── synex-api-gateway-service/
    ├── synex-user-service/
    └── synex-deployment/

Before starting the infrastructure, make sure the `.env.local` files in the individual service repositories are created and configured based on their respective `.env.example` files.

Then, in this repository, create a `.env.local` file based on `.env.example` and fill in the required variables.

Start the local environment:

    docker compose --env-file .\.env.local up --build

Stop the environment and remove volumes:

    docker compose down -v

## Deployment

This repository contains the deployment configuration for the Synex application.

Deployment configurations for different environments and platforms, such as VPS and Kubernetes, will be maintained here.
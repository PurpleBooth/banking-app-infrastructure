# Banking App Infrastructure

## Contents

This repository contains the Kubernetes configuration for shared infrastructure
used by the microservices. This includes:

- The [RabbitMQ](https://www.rabbitmq.com/) message broker
- The Ingress API routes

## Deploying

### 1. Update the hosts in the [ingress.yml](./kubernetes/ingress.yml)

For the app, use `banking-app.apps.example.com`.

For the RabbitMQ dashboard use `banking-rabbit.apps.example.com`.

### 2. Deploy

`kubectl -n NAMESPACE apply -f kubernetes/`

Note: There is an included [Jenkinsfile](./Jenkinsfile) which allows this step
to be done via a pipeline.

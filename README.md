# simple_K8S_project
This project demonstrates how to deploy a simple web application using MongoDB, Kubernetes, and Minikube. The application is hosted on a local Kubernetes cluster managed by Minikube.

## Prerequisites

- [Docker](https://www.docker.com/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [MongoDB](https://www.mongodb.com/)

## Setup Instructions

### 1. Install and Start Minikube

Install Minikube in its official page

Start Minikube with the following command:
```bash
minikube start
```
### 2. Apply Kubernetes Configurations

Apply ConfigMap

Create a ConfigMap for the MongoDB configuration:

Apply the ConfigMap
```bash
kubectl apply -f (configmap_file_name)
```
Create a Secret for MongoDB credentials:

Apply the SecretFile
```bash
kubectl apply -f (secret_file_name)
```
Create a Deployment and Service for MongoDB:

Apply the Deployment and Service file for MongoDB
```bash
kubectl apply -f (mongo_file_name)
```
Create a Deployment and Service for the web application:

Apply the Deployment and Service for the web application
```bash
kubectl apply -f (webapp_file_name)
```

### 3. Accessing the Application

After deploying the services, you can access the web application by exposing the web service:
```bash
minikube service webapp-service
(or)
minikube ip
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

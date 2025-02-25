# Docker Container for a Simple Web Application

This repository contains a simple Flask web application containerized using Docker.

## Features
- Flask web application (`app.py`)
- Dockerfile to build and run the app in a container
- Instructions for building and running the container

## Getting Started

### Prerequisites
- [Docker](https://www.docker.com/) installed
- [Git](https://git-scm.com/) installed

### Clone the Repository
```bash
git clone https://github.com/elogonyi/Docker-container-for-a-simple-web-application.git
cd Docker-container-for-a-simple-web-application
Build and Run the Docker Container
Build the Docker image
bash
Copy
Edit
docker build -t flask-docker-app .

Build and Run the Docker Container
Build the Docker image
bash
Copy
Edit
docker build -t flask-docker-app .
Run the container
bash
Copy
Edit
docker run -p 5000:5000 flask-docker-app
Access the Application
Open your browser and go to http://localhost:5000

Kubernetes Deployment (Optional)
To deploy this application using Kubernetes, create and apply a deployment file:

yaml
Copy this

apiVersion: apps/v1
kind: Deployment
metadata:
  name: flask-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: flask-app
  template:
    metadata:
      labels:
        app: flask-app
    spec:
      containers:
        - name: flask-app
          image: flask-docker-app
          ports:
            - containerPort: 5000
Apply the deployment:

bash
Copy

kubectl apply -f deployment.yaml

Author
elogonyi


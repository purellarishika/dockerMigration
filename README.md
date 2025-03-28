Step-by-Step Plan

Create Project Folder and Files

	Create a folder named my-docker-image at D:\my-docker-image.
	Inside this folder, create a file named index.js for the Express server.
	Create a Dockerfile to define the containerization process.

Implement Express Server

	Write the Express server code in index.js to serve "Hello from Docker in VS Code!" on port 3000.

Create Dockerfile

	Define the Dockerfile to build a custom Docker image from the official node:16 base image.

Build and Push Docker Image

	Build the Docker image and push it to Docker Hub with the tag 10tf1a0234/my-docker-image:latest.
	#docker build -t 10tf1a0234/my-docker-image:latest .
	#docker push 10tf1a0234/my-docker-image:latest

Setup Kubernetes and Helm Chart

	Create a helm-chart subdirectory in D:\my-docker-image.
	Define the Helm chart to configure Deployment, Service, Ingress, and HPA.

Deploy to Kubernetes

	Use Helm to deploy the application to a local Kubernetes cluster on Docker Desktop.
	Ensure Docker Desktop is running with Kubernetes enabled
	#helm install my-docker-image ./helm-chart

Ensure the application is accessible at http://myapp.local:30183 and http://localhost:30183.

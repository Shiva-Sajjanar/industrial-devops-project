# Industrial Equipment Website — DevOps CI/CD Project

## Project Overview

This project demonstrates a simple industrial equipment website deployed using Docker and an automated Jenkins CI/CD pipeline.

The website represents a demo industrial equipment company that provides electrical panels and industrial automation solutions.

## Technologies Used

* HTML and CSS
* Git and GitHub
* Linux (Ubuntu)
* Docker
* Jenkins
* Nginx
* Jenkins Pipeline
* Polling SCM

## Project Features

* Created a demo industrial equipment website.
* Stored source code in a GitHub repository.
* Built a Docker image using a Dockerfile.
* Configured a Jenkins pipeline to check out source code from GitHub.
* Automated Docker image building.
* Automated container deployment.
* Configured Jenkins Polling SCM to detect changes in the GitHub repository.

## CI/CD Workflow

1. Developer updates the website source code.
2. Changes are committed and pushed to GitHub.
3. Jenkins checks the repository for changes using Polling SCM.
4. Jenkins checks out the latest source code.
5. Jenkins builds the Docker image.
6. Jenkins replaces the previous demo container with a new container.
7. The website is served by Nginx.

## Project Structure

```text
industrial-devops-project/
├── Dockerfile
├── index.html
└── README.md
```

## Docker Configuration

The Docker image is built using Nginx Alpine.

```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```

## Run the Website Locally

Build the image:

```bash
docker build -t industrial-website:v2 .
```

Run the container:

```bash
docker run -d --name industrial-website-v2 -p 8087:80 industrial-website:v2
```

Open the website in your browser:

`http://localhost:8087`

## Jenkins Pipeline Stages

1. Checkout source code from GitHub.
2. Check project files.
3. Build the Docker image.
4. Deploy the website container.

## Learning Outcomes

* Git version control
* GitHub repository management
* Docker image and container management
* Jenkins pipeline configuration
* CI/CD automation
* Automated container deployment

## Disclaimer

This is a learning and portfolio project. The website is a demonstration and is not connected to a production industrial equipment company's systems.

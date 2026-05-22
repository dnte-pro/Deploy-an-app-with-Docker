🚀 Containerized Web App Deployment on AWS Elastic Beanstalk

This project demonstrates how to containerize a simple web app with Docker and deploy it on AWS Elastic Beanstalk for global accessibility.

📌 Project Overview

The goal of this project was to:

Build a lightweight web application.

Package it inside a Docker container.

Deploy the containerized app to AWS Elastic Beanstalk for scalable, managed hosting.

By leveraging Docker and AWS, the application became portable, reproducible, and cloud-ready.

🛠️ Tech Stack

Docker – Containerization

Nginx – Web server

AWS Elastic Beanstalk – Application deployment & scaling

Amazon EC2 (behind the scenes) – Managed compute infrastructure

Elastic Load Balancing (ELB) – Traffic distribution

Amazon S3 – Stores deployment package


Elastic Beanstalk provisions the required infrastructure and makes the app available online.

📂 Project Structure
aws-docker-webapp/
│── Dockerfile
│── index.html


🚀 Deployment Flow

Develop app locally →

Containerize with Docker →

Deploy via Elastic Beanstalk →

AWS provisions infrastructure →

Access app globally 🌍

📚 Key Learnings

Docker simplifies app packaging and portability.

Elastic Beanstalk abstracts away server management.

Together, they provide a smooth Dev → Deploy → Scale pipeline.

🔮 Improvement ideas

Add CI/CD using AWS CodePipeline + CodeBuild.

Support multi-container deployments with ECS/Fargate.

Integrate monitoring with CloudWatch.


🤝 Connect

💬 If you’re working with Docker, AWS, or Elastic Beanstalk, let’s connect and share learnings!

---




---




---
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Deploy an App with Docker

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-eb)

**Author:** Kiprono Yegon  
**Email:** kipronoyegon50@gmail.com

---

![Image](http://learn.nextwork.org/inspired_gray_mysterious_dragon/uploads/aws-compute-eb_c4df13c84)

---

## Introducing Today's Project!

### What is Docker?

Docker is an open-source platform that lets you build, package, and run applications inside containers that contains everything an app needs: code, runtime, libraries, and dependencies.
We used Docker to package everything our application needed.

### One thing I didn't expect...

The project is quite simple when youu have a look at it at the end, but a small mistake a long the way can cost you your time trying to trouble shoot it

### This project took me...

I took quite a long while completing the project because of the errors I encounterd and some unavoidable circumstances (we are just but human). However I managed it in the end :)

---

## Understanding Containers and Docker

### Containers

containers are packages which dependencies of a given software are packaged. They are useful because they package all the necessities of a software needs

A container image is a template for containers that tell Docker what to include in a container such as application code , libraries and dependencies.

### Docker

DOcker is a too for container management.Docker Desktop is an app that makes using docker more interactive and efficient.

The docker daemon is a background process that manages the Docker containers on your computer

---

## Running an Nginx Image

Nginx is a web server which handles web traffic smoothly and efficiently. It is also a 'proxy server' which means it forwards requests from the internet to other servers.

The command I ran to start a new container was "docker run -d -p 80:80 nginx"

![Image](http://learn.nextwork.org/inspired_gray_mysterious_dragon/uploads/aws-compute-eb_6245f5bb10)

---

## Creating a Custom Image

The Dockerfile is a document with instructions for building your image.

My Dockerfile tells docker three things: that it has to copy the latest nginx image and also replaces the default HTML file with the provided html file and lastly to enable traffic through port 80

The command I used to build a custom image with my Dockerfile was docker build -t my-web-app .  The '.' at the end of the command means that the Dockerfile is in the directory we are in "Compute"

![Image](http://learn.nextwork.org/inspired_gray_mysterious_dragon/uploads/aws-compute-eb_4c741d1913)

---

## Running My Custom Image

There was an error when I ran mycustom imagge because there was another container running using the port 80. I resolved this by stopping the running container and rerun my container and voila, it works.

In this example, the container image is the one that directs the Docker of what should get into the container i.e the application code, dependencies, libraries etc . The container is the actual software that is created from the image

![Image](http://learn.nextwork.org/inspired_gray_mysterious_dragon/uploads/aws-compute-eb_74b5c3d619)

---

## Elastic Beanstalk

Elastic Beanstalk is a cloud service that is fully managed and it enables you to deploy cloud applications without worrying of the underlying infrastructure you just upload you code and it handles setting servers and autoscaling

Deploying my custom image with Elastic Beanstalk took me aa while because of the error I encountered. I had to consult in communities and other peers who were helpful and insightful on how to come around the issues I faced.

![Image](http://learn.nextwork.org/inspired_gray_mysterious_dragon/uploads/aws-compute-eb_26d5573b23)

---

## Deploying App Updates

---

---

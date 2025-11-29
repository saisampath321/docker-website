🚀 Docker Website Deployment on AWS EC2

This project demonstrates how to deploy a simple static website using Docker and Nginx on an AWS EC2 instance.
It is part of my DevOps learning path (Project 3).


---

📌 Project Overview

In this project, I:

Created a static HTML webpage (index.html)

Wrote a Dockerfile using the official Nginx image

Built a custom Docker image

Deployed the website inside a container

Exposed the container on EC2 using port mapping

Configured AWS Security Groups to allow traffic

Accessed the website using the EC2 public IP


This project shows my understanding of Docker, containers, Dockerfiles, Linux commands, and AWS EC2 networking.


---

📁 Project Structure

docker-website/

│── Dockerfile
│── index.html


---

🛠 Technologies Used

Docker

Dockerfile

Nginx

AWS EC2 (Amazon Linux)

Linux / Bash

Networking (Ports, Security Group Rules)



---

📄 Dockerfile

FROM nginx:latest
COPY . /usr/share/nginx/html


---

🌐 How to Run This Project (Step-by-Step)

1️⃣ Install Docker on EC2

sudo yum update -y
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user

Reconnect SSH.


---

2️⃣ Clone or upload project files to EC2

cd docker-website


---

3️⃣ Build Docker image

docker build -t docker-website .


---

4️⃣ Run Docker container

docker run -d -p 8080:80 docker-website


---

5️⃣ Open website in browser

http://3.26.255.41/:8080

Make sure port 8080 is allowed in the EC2 security group.

🧑‍💻 Author

Sai Sampath
DevOps & Cloud Enthusiast

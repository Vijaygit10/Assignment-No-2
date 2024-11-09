Dockerized Nginx Project to GitHub

Step 1: Set Up the Project Directory
Create a New Directory for Your Project: Open your terminal and run the following commands:

bash

mkdir my-nginx-app
cd my-nginx-app

Create a Dockerfile: In the my-nginx-app directory, create a file named Dockerfile with the following content:

Dockerfile

# Use the official Nginx image from the Docker Hub
FROM nginx:alpine

# Copy the HTML files to the appropriate directory
COPY ./html /usr/share/nginx/html

# Expose port 80 for the web service
EXPOSE 80
Create an HTML Directory and a Sample HTML File:

bash

mkdir html
Create index.html: In the html directory, create a file named index.html with the following content:

html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Nginx Server</title>
</head>
<body>
    <h1>Welcome to My Nginx Server!</h1>
</body>
</html>

Step 2: Build the Docker Image
Build the Docker Image: In the terminal, run the following command:

bash

docker build -t my-nginx-app .

Step 3: Run the Docker Container
Run the Docker Container: Execute the following command:
bash

docker run -d -p 8080:80 my-nginx-app

This will run your Docker container in detached mode and map port 8080 on your host machine to port 80 in the container.

Step 4: Accessing the Service
Open Your Web Browser: Navigate to:
text

http://localhost:8080
You should see a page displaying "Welcome to My Nginx Server!".
Step 5: Documenting the Project
Create a README.md File: In the my-nginx-app directory, create a file named README.md with the following content:

# My Nginx App

This is a basic Dockerized Nginx server setup.

## Prerequisites

- Docker must be installed on your machine.

- ## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/my-nginx-app.git
   cd my-nginx-app
Build the Docker image:

bash

docker build -t my-nginx-app .
Run the Docker container:

bash

docker run -d -p 8080:80 my-nginx-app
Access the service: Open your browser and visit http://localhost:8080

Stopping the Container
To stop the running container, find the container ID using:

bash

docker ps
Then run:

bash

docker stop 

License
This project is open-source.


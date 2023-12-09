video: https://youtu.be/nTzC6gxNGZU
# Azure-Flask-App

This README will guide you through the process of creating an auto-scaling application using GitHub, Docker, and Microsoft App Services.

## Step One: Environment Set Up
Begin by setting up your environment using GitHub Code Spaces and VS Code.


## Step Two: Flask App
Build a basic Flask application. Ensure to include the host and port number in your configuration. You can start with my example or find more sophisticated ones online. The primary goal is to establish the underlying infrastructure.

## Step Three: Build Docker File
Use the provided template for your Docker file. Remember to expose port 5000.
Commands to use:
  - `docker build app-name .`
  - `docker run -p 5000:5000 app-name`

## Step Four: Login to DockerHub via Codespaces
Enter `docker login --username=XXXX` in the terminal. Build your container and push it to DockerHub (create your DockerHub repository first).
Commands:
  - `docker login --username=`
  - `docker build -t username/repo .`
  - `docker push username/repo`

Ensure you create the repository with the necessary title before pushing.


## Step Five: Setup via Azure App Services
In Azure App Services configuration settings, add "WEBSITES_PORT" with a value of 5000.

### Step Five a)
Log into Azure, search for app services, and choose to create a web app.


### Step Five b)
While creating the app, select the Docker Container option. Be aware of naming conventions.


### Step Five c)
Select the correct image tab when choosing your Docker container.


### Step Five d)
Post-deployment, go to configuration settings and add "WEBSITES_PORT" with a value of 5000. This enables your app to run at the public URL provided by Azure.


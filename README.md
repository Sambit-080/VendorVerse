# VendorVerse

A web application for managing vendors, built with Node.js and Express.

## Prerequisites

To run this project, you will need [Docker](https://www.docker.com/get-started) installed on your machine.

## Deployment with Docker

You can easily build and run this application as a Docker container.

### 1. Build the Docker Image

Navigate to the root directory of the project in your terminal and run the following command. This will build the Docker image and tag it as `vendorverse`.

```sh
docker build -t VendorVerse .
```

### 2. Run the Docker Container

After the image has been successfully built, run the following command to start the application in a container. This will map port 3000 on your local machine to port 3000 inside the container.

```sh
docker run -p 3000:3000 VendorVerse
```

The application will now be running and accessible at http://localhost:3000.

## Available Routes

The application has the following routes available:

*   `GET /`: The home page.
*   `GET /dashboard`: The application dashboard.
*   `GET /users`: A sample route for user information.

## Project Structure

A brief overview of the key files and directories:

```
├── Dockerfile          # Defines the Docker image for the application.
├── app.js              # The main Express application configuration file.
├── bin/www             # The executable script that starts the Node.js server.
├── package.json        # Lists project dependencies and scripts.
├── public/             # Contains static assets (CSS, images, etc.).
├── routes/             # Contains the route definitions for the application.
└── views/              # Contains the EJS view templates.
```
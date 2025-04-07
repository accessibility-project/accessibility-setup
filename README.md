# Accessibility Website - Docker Setup

This project consists of a frontend application and a backend API service. Docker is used to run both services together.

## Services
There are two main services:

1. Frontend:

- Built from the accessibility-focused-website directory.

- Exposes port 3000 for frontend development.

- Uses CHOKIDAR_USEPOLLING=true to handle file changes in development mode.

- Depends on the backend service to fetch data.

2. Backend:

- Exposes port 5000 to provide API services for the frontend application.

## Prerequisites
Docker and Docker Compose must be installed on your machine.

## Installation
### Step 1: Clone the repositories
Clone the necessary repositories to your local machine.

`git clone https://github.com/accessibility-project/accessibility-focused-website`

`git clone https://github.com/accessibility-project/news-api`

`git clone https://github.com/accessibility-project/accessibility-setup`

`cd accessibility-project`

### Step 2: Build and start the services using Docker Compose
Build and start the services (frontend and backend) using Docker Compose:

`docker-compose up --build`

This will:

- Build both the frontend and backend services.

- Start the frontend on port 3000 and the backend on port 5000.

### Step 3: Access the application
The frontend application should now be available at:

http://localhost:3000

The backend API is available at:

http://localhost:5000

## Services Overview:
### Frontend:

- Built from ../accessibility-focused-website.

- Exposes port 3000 to serve the user interface.

- Waits for the backend service to display dynamic content.

### Backend: 

- Built from ../news-api.

- Exposes port 5000 to serve API data.

## Notes
- Ensure you have Docker and Docker Compose installed before starting the services.

- The frontend depends on the backend, so Docker Compose ensures the backend starts first.


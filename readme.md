# EdTech_Platform

Learnify is a comprehensive course recommendation platform designed to help users achieve their learning goals efficiently. The platform, built with Angular and Node.js, incorporates AI and data science functionalities using Python and Flask. PostgreSQL is employed as the database, and the entire application is containerized using Docker. For those interested in container orchestration, Kubernetes manifests are also provided.

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Local Setup](#local-setup)
  - [Docker Usage](#docker-usage)
  - [Kubernetes Deployment](#kubernetes-deployment)
- [Website Demonstration](#website-demonstration)
- [UI Preview](#ui-preview)

## Introduction

Learnify is a course recommendation platform that enables users to input learning preferences, budget constraints, and weekly time commitments. Leveraging AI and data science, the platform generates a master course—a curated set of courses tailored to the user's objectives. The technology stack includes Angular for the frontend, Node.js for the backend, Python and Flask for AI/data science, and PostgreSQL as the database. Docker is employed for seamless deployment and scaling, with optional Kubernetes support.

## Getting Started

### Prerequisites

Before starting, ensure you have the following installed:

- Node.js
- Angular CLI
- Python
- Flask
- PostgreSQL
- Docker (optional)
- Kubernetes (optional)

### Local Setup

1. **Install frontend and backend dependencies:**

   ```bash
   # Install frontend dependencies
   cd client
   npm install

   # Install backend dependencies
   cd ../server
   npm install

2. **Install Python Dependencies:**
    Ensure you have the required Python dependencies installed for the AI/model component:

    ```bash
    # Install Python dependencies
    cd ../model
    pip install -r requirements.txt

3. **Create a .env file in the server folder with the following content:**

    ```bash
    MODEL_API=<model api>
    POSTGRESQL_DB_HOST = <host>
    POSTGRESQL_DB_USER = <username>
    POSTGRESQL_DB_PASSWORD = <password>
    POSTGRESQL_DB = <database name>


4. **Create an environment.ts file in the client/src/environments folder with the following content:**

    ```bash
    export const environment = {
    production: false,
    apiUrl: 'http://localhost:3000', // Adjust if necessary
    };

5. **Start the backend server:**

    ```bash
    cd server
    node index

6. **In a separate terminal, start the Angular frontend:**

    ```bash
    cd client
    ng serve


7. **Open your browser and navigate to http://localhost:4200 to access Learnify**

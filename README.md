# Teachers and Courses API

This project implements a JSON API server for managing teachers and courses. It provides endpoints to create, retrieve, and filter teacher and course records. The data is stored in a MySQL database, and the entire application is containerized using Docker to ensure easy setup and deployment.

# Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Documentation](#documentation)
- [Testing](#testing)

# Features

- Create new teacher records with a unique teacher ID, name, active status, and designation.
- Retrieve teacher records by ID and filter teachers based on various attributes.
- Create new course records with a unique course ID, course mentor (teacher ID), name, start date, end date, description, and active status.
- Retrieve course records by ID and filter courses based on various attributes.
- Entire application and database can be run using Docker Compose.

## Getting Started

### Prerequisites

To run this application, you need to have the following installed on your system:

- Docker: [Install Docker](https://www.docker.com/get-started)

### Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your_username/teachers-courses-api.git
   cd teachers-courses-api
   ```

2. Build the Docker containers:

   ```bash
   docker-compose build
   ```

3. Start the Docker containers:

   ```bash
   docker-compose up -d
   ```

   The API server will be accessible at `http://localhost:8080`.

## API Endpoints

The API provides the following endpoints:

### Teachers

- **POST /teacher**: Create a new teacher record with the given JSON payload.
- **GET /teacher/{id}**: Get a specific teacher record by ID.
- **GET /teacher**: Get a list of teachers based on filters.

### Courses

- **POST /course**: Create a new course record with the given JSON payload.
- **GET /course/{id}**: Get a specific course record by ID.
- **GET /course**: Get a list of courses based on filters.

## Documentation

For detailed documentation of the API endpoints and example requests and responses, please refer to the [API Specification](api-specification.md) file.

## Testing

You can test the API using `curl` or any other HTTP client of your choice. Sample test cases and example `curl` commands can be found in the [Sample Test Cases](sample-test-cases.md) file.

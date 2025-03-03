# Task1


## Requirements

- [Docker](https://www.docker.com/products/docker-desktop) (with Docker Compose)
- [Git](https://git-scm.com/)
- [Maven](https://maven.apache.org/) (for local builds, if necessary)

## Setup and Run

### 1. Clone the repository

```bash
git clone https://github.com/st1gmat/docker_practice.git
cd demo-app
```

### 2. Build and run the containers

```bash
docker-compose up --build
```

This will:
1. Build the project using Maven.
2. Launch two containers: MySQL and Spring Boot application.
3. Access the app at [http://localhost:8080](http://localhost:8080), and MySQL will be available at port 3306.

### 3. Test the API

Once the containers are running, you can test the API using curl or Postman

**Add a user:**

```bash
curl -X POST -H "Content-Type: application/json" -d '{"name": "Ilya"}' http://localhost:8080/users
```

**Get all users:**

```bash
curl -X GET http://localhost:8080/users
```

### 4. Stop the containers

```bash
docker-compose down
```

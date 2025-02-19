# Demo Spring Boot Application

This is a demo project for Spring Boot that manages student information. It includes basic CRUD operations for students.



## Prerequisites

- Java 17 or higher
- Maven 3.9.9 or higher
- PostgreSQL database

## Database Setup
Before running the application, you need to create a student database in PostgreSQL:

```CREATE DATABASE student;```

## Configuration

The application uses PostgreSQL as the database. Update the database configuration in `src/main/resources/application.properties` if necessary:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/student
spring.datasource.username=postgres
spring.datasource.password=1234
spring.jpa.hibernate.ddl-auto=create-drop
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

server.error.include-message=always
```

## API Endpoints
The application exposes the following REST API endpoints:

```
GET /api/v1/student: Get all students

POST /api/v1/student: Register a new student

DELETE /api/v1/student/{studentId}: Delete a student by ID

PUT /api/v1/student/{studentId}: Update a student's name and/or email
```
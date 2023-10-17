# Rocketseat Java project

## Description

This repository contains a Java project build with the Spring framework. The project was developed in a Rocketseat Java course, and it serves as a task management system, offering features for user registration, task creation, listing, updating, and user authentication.

## Deployment
You can access the deployed version of this project by following this link: https://rocketseat-todolist-94en.onrender.com

## Tech Stack
The project incorporates the following technologies and dependencies:

- **Spring Boot**: The core framework for building the application.
- **Spring Boot DevTools**: A development tool that helps with auto-restarting the server during development.
- **Spring Boot Starter Web**: A starter for building web applications using Spring MVC.
- **Spring Boot Starter Test**: Provides testing support for the application.
- **Spring Boot Starter Data JPA**: For data access and persistence using Java Persistence API (JPA).
- **H2 Database**: An in-memory database used for development and testing.
- **Lombok**: A library for reducing boilerplate code in Java.
- **Bcrypt**: A library for secure password hashing.
- **Docker**: Used for containerization, making it easier to deploy and manage the application in different environments.


## Endpoints
Here are the primary endpoints in this project:

1. **User Registration:**
   - Description: Allows users to register by providing their username, name, and password.
   - Method: POST
   - URL: `/users/`
   - Request Example:
      ```json
     {
         "name": "x",
         "username": "x",
         "password": "x"
     }
      ```
   - Response Example: Returns the created user if registration is successful.

2. **Task Creation:**
   - Description: Allows users to create tasks, specifying the title, description, start date, end date, and priority.
   - Method: POST
   - URL: `/tasks/`
   - Request Example:
     ```json
     {
         "title": "Task Title",
         "description": "Task Description",
         "startAt": "2023-10-18T08:00:00",
         "endAt": "2023-10-19T17:00:00",
         "priority": "High"
     }
     ```
   - Response Example: Returns the created task if creation is successful.
   - Authentication: Basic Authentication required.

3. **Task Listing:**
   - Description: Lists all tasks associated with the authenticated user.
   - Method: GET
   - URL: `/tasks/`
   - Request Example: Send a GET request to retrieve a list of tasks for the authenticated user.
   - Response Example: Returns a list of tasks.

4. **Task Update:**
   - Description: Allows users to update the details of an existing task.
   - Method: PUT
   - URL: `/tasks/{id}`
   - Request Example:
     ```json
     {
         "title": "Updated Task Title"
     }
     ```
   - Response Example: Returns the updated task if the operation is successful.
   - Authentication: Basic Authentication required.

**Please note that authentication is required for task-related endpoints. User authentication is achieved through Basic Authentication using the Authorization header.**

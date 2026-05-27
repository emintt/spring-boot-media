# Spring Boot Media API

Spring Boot Media is a REST API built with Spring Boot, Java 21, and MariaDB. The application manages users and media items and exposes CRUD endpoints for both resources.

## Documentation

- https://java-spring-boot-api-liemnguyen.netlify.app/
- The generated API specification is based on [src/main/resources/data/api-docs.yaml](src/main/resources/data/api-docs.yaml).

## Tech Stack

- Java 21
- Spring Boot 3.2.x
- Spring Web
- Spring Data JDBC
- Spring Validation
- MariaDB
- springdoc-openapi

## Features

- List, create, update, and delete users
- List, create, update, and delete media items
- Fetch media items by user id
- Validation for incoming user and media payloads
- OpenAPI documentation for the REST endpoints

## API Endpoints

Base path:

- `/api/user`
- `/api/media`

User endpoints:

- `GET /api/user`
- `GET /api/user/{id}`
- `POST /api/user`
- `PUT /api/user/{id}`
- `DELETE /api/user/{id}`

Media endpoints:

- `GET /api/media`
- `GET /api/media/{id}`
- `GET /api/media/user/{id}`
- `POST /api/media`
- `PUT /api/media/{id}`
- `DELETE /api/media/{id}`

## Project Files

- Application entry point: [src/main/java/application/media/Application.java](src/main/java/application/media/Application.java)
- Media controller: [src/main/java/application/media/media/MediaController.java](src/main/java/application/media/media/MediaController.java)
- User controller: [src/main/java/application/media/user/UserController.java](src/main/java/application/media/user/UserController.java)
- OpenAPI definition: [src/main/resources/data/api-docs.yaml](src/main/resources/data/api-docs.yaml)
- SQL schema: [src/main/resources/schema.sql](src/main/resources/schema.sql)
- Sample data: [src/main/resources/data/db.sql](src/main/resources/data/db.sql)

## Running Locally

1. Start MariaDB and create the `MediaApp` database.
2. Make sure the credentials in `application.properties` match your local database.
3. Run the app with Maven:

```bash
./mvnw spring-boot:run
```

On Windows, you can use:

```bash
mvnw.cmd spring-boot:run
```

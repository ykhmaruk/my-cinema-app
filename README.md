# <div align="center">🎥 СINEMA-APP 🎥</div>

REST web application for ticket reservation. It
implements the main functions, such as:
- displaying movies that are currently at the box office;
- shopping cart with the ability to add tickets to it and create
an order based on the added tickets;
- searching for available movie sessions by date.

## Project structure:
- DAO (Data Access Object) - DAO is the data access layer responsible for interacting with the database. This layer
  implements operations related to retrieving, storing, updating, and deleting data.
- Service - The service layer is responsible for the business logic of the application. It handles data processing,
  executes business rules, and coordinates actions between the DAO and other components of the application.
- Controller - The Controller layer serves as the entry point for external requests to the application.

## Entities relations diagram:
![cinema-app schema](/images/schema.png)

## Endpoints:
User and Admin:
- GET: /cinema-halls - display cinema halls;
- GET: /movies - display movies;
- GET: /movie-sessions/available - display available movie sessions;

User-only:
- GET: /orders - display all user orders;
- GET: /shopping-carts/by-user - display user shopping cart;
- POST: /orders/complete - complete an order;
- PUT: /shopping-carts/movie-sessions - add a movie session to the shopping cart;

Admin-only:
- DELETE: /movie-sessions/{id} - delete movie session;
- GET: /users/by-email - find user by email;
- POST: /cinema-halls - add a new cinema hall;
- POST: /movies - add a new movie;
- POST: /movie-sessions - add a new movie session;
- PUT: /movie-sessions/{id} - update a movie session.

## Used technologies:
- Java 17
- Spring 5.3.20
- Spring-Web 5.3.20
- Spring-Security 5.6.10
- Hibernate 5.6.14.Final
- MySQL 8.0.22
- Apache TomCat 9.0.76
- Maven 4.0

## Instructions for launching the project:
1. Clone the project from GitHub;
2. Install Apache Tomcat version 9.x.x.;
3. Install MySql;
4. Install Postman for sending requests;
5. Congigure db.properties with correct data; 
6. Add TomCat configuration; 
7. Run the project.
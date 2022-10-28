# :cinema: Cinema :cinema:

## :key:  About

This application represent a cinema ticket selling service.
The application is intended for use by cinema halls admins and their user.

## :mag:  Details

The user can register, add a ticket to the cart, buy a ticket and get information about the session. 
Users have the opportunity to see what films are shown in a particular cinema, with the ability to view 
descriptions of films and descriptions of cinema halls.

Admins have the opportunity to add a cinema halls, a movie and a movie session. Can view visitor information. 

## :scroll:  Project Structure

In this project used the n-tier architecture

- DAO tier - allows to modify data in database using CRUD methods
- Service tier - this is where all the logic happens
- Controller tier - provides an interface to interact with application

#### __All visitors can:__

- __GET__
  - log in `GET: /login`
  - logout `GET: /logout`
- __POST__
  - register `POST: /register` 


#### __ADMIN can:__

- __GET:__
  - user by __email__ `GET: /users/by-email`
  - movies `GET: /movies`
  - cinema halls `GET: /cinema-halls`
  - available movie sessions `GET: /movie-sessions/available`
  - certain movie session `GET: /movie-sessions/{id}`
- __POST:__
    - movies `POST: /movies`
    - cinema halls `POST: /cinema-halls`
    - movie sessions `POST: /movie-sessions`
- __PUT:__
    - certain movie session `PUT: /movie-sessions/{id}`
- __DELETE:__
    - certain movie session `DELETE: /movie-sessions/{id}`

#### __USER can:__

- __GET:__
  - orders `GET: /orders`
  - cinema halls `GET: /cinema-halls`
  - movies `GET: /movies`
  - available movie sessions `GET: /movie-sessions/available`
  - certain movie session `GET: /movie-sessions/{id}`
  - shopping carts by user `GET: /shopping-carts/by-user`
- __POST:__
  - orders `POST: /orders/complete`
- __PUT:__
  - tickets to shopping cart for some movie session `PUT: /shopping-carts/movie-sessions`

>HINT: for testing you can use [Postman](https://web.postman.co/) and write request in the body

## :hammer_and_wrench:  Technologies

- MySQL 8.0.30
- Apache Maven 3.8.5
- Java 11 
- Hibernate
- Spring Core
- Spring ORM
- Spring Web MVC
- Spring Security
- Apache TomCat 9.0.50

## :gear:  How to launch

- Download and install [MySQL](https://dev.mysql.com/downloads/installer/)
- Download and extract [Maven](https://maven.apache.org/download.cgi)
- Download and extract [Tomcat 9.0.50](https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.50/bin/)
- Fork this project to your repository
- Clone it to your PC and open it in IDE
- Configure db.properties in "resources" folder
- Create new schema in MySQL
- Change the configuration to use "Tomcat Server Local"
- Run the project :rocket:

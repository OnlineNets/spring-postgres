# Welcome to spring-boot-postgres Sample project

## Pre requisities
Java 8
Maven 3.1.x
Postgresql instance

## Postgres Instance Configuration
In order to use your instance please update postgres.properties
```
spring.jpa.database=POSTGRESQL
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=create-drop
spring.database.driverClassName=org.postgresql.Driver
spring.datasource.url=jdbc:postgresql://localhost:5432/blood
spring.datasource.username=postgres
spring.datasource.password=postgres
```

## Run Application Locally
```mvn spring-boot:run```

to add a user make a POST like this example : ```http://localhost:9095/user/Yazid Cherfi```

to list all application users : ```http://localhost:9095/user```

## Load Sample Data
schema and data are initialized using ```schema-${platform}.sql``` and ```data-${platform}.sql```

## Invoke Application

### Add a user
```curl -X POST "http://localhost:9095/user/Abderrazak BOUADMA"```
running the above POST request will result to an 200 Ok HTTP response and JSON Content-Type of Application/json of the new created object.

### List All Users
```curl "http://localhost:9095/user"```
running the above GET request will result to an 200 Ok HTTP response and JSON Content-Type of Application/json and a list (maybe empty) of all users in DB


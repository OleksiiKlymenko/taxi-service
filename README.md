# Taxi-Service

---

## Description
This application simulates the operation of a taxi service 
in which we can perform various actions with drivers, 
cars and car manufacturers. In this implementation, the user is the driver, so he can
log in, log out.

---

## What you can do in this App?
* Authentication (Log in and log out)
* Add or delete manufacturers
* Add or delete cars
* Add or delete drivers
* Add drivers to specific car
* Display all cars of current authenticated driver
* Display all cars, manufacturers and drivers

---

## Structure

*The project has 3-Tier Architecture*

1. **DAO**
   - CarDaoImpl - get access to car model from DB 
   - ManufacturerDaoImpl - get access to manufacturer model from DB 
   - DriverDaoImpl - get access to driver model from DB
2. **SERVICE**
    - CarServiceImpl - processes car's CRUD logic
    - DriverServiceImpl - processes driver's CRUD logic
    - ManufacturerServiceImpl - processes manufacturer's CRUD logic
    - AuthenticationServiceImpl - processes authentication logic
3. **CONTROLLER**
    - Authentication controllers:
        - LoginController - to log in
        - LogoutController - to log out
    - Car controllers:
        - AddCarController - to create new car
        - DeleteCarController - to delete car
        - GetAllCarsController - to show all cars
        - AddCarController - to create new car
    - Driver controllers:
        - AddDriverController - to register driver
        - DeleteDriverController - to delete driver
        - GetMyCurrentCarsController - to show all cars of current registered driver
        - GetAllDriversController - to show all drivers
    - Manufacturer controllers:
        - AddManufacturerController - to create new manufacturer
        - DeleteManufacturerController - to delete manufacturer
        - GetAllManufacturersController - to show all manufacturers
    - IndexController - homepage

---

## Technologies 

- **Java 11**
- **Maven 4.0.0 version**
- **MySql 8.0.22 version**
- **Jakarta servlet 6.0.0 version**
- **Apache Tomcat 10.1.7 version**
- **JSTL 1.2 version**

---

## How to run?
- Clone this repository using SSH `git@github.com:OleksiiKlymenko/taxi-service.git`
- Initialize the database by using SQL script : `src/main/resources/init_db.sql`
- Update fields `JDBC_DRIVER`, `URL`, `USERNAME`, `PASSWORD` with your database connection information in `src/main/java/taxi/util/ConnectionUtil.java`
- Configure Tomcat 

# Author
Oleksii Klymenko

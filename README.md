# BookingSystem

# Build a Service that track overstay fees in a hospitality system

# Spring Boot, MySQL, Spring Security, JWT, JPA, Rest API

## Steps to Setup


**1. Unzip the file**


**2. Create Mysql database**
```bash
create database bookingdb
```
- run Please note that once the application has been started the tables will be created in the db

**3. Change mysql username and password as per your installation**

+ open `src/main/resources/application.properties`
+ change `spring.datasource.username` and `spring.datasource.password` as per your mysql installation

**4. Run the app using maven**

```bash
mvn spring-boot:run
```
The app will start running at <http://localhost:9080>

## Explore Rest APIs using postman or swagger

### Swagger:  Swagger API specification is available at http://localhost:8090/swagger-ui/. The server has to be up and running in for the documentation to be available


### Authentication

| Method | Url | Decription | Sample Valid Request Body | 
| ------ | --- | ---------- | --------------------------- |
| POST   | /api/auth/signup | Sign up | [JSON](#sign-up) |
| POST   | /api/auth/login | Log in | [JSON](#login) |

### User

| Method | Url | Description | Sample Valid Request Body |
| ------ | --- | ----------- | ------------------------- |
| GET    | /api/me | Get current user details | |


### RoomType

| Method | Url | Description | Sample Valid Request Body |
| ------ | --- | ----------- | ------------------------- |
| GET    | /api/me/roomTypes | Get room types that belong to current customer | |
| GET    | /api/me/{id} | Get post by id | |
| POST   | /api/me/roomTypes | Create a room type |
| PUT    | /api/me/roomTypes/{roomTypeId} | Update a room type |
| DELETE | /api/me/roomTypes/{roomTypeId} | Delete a room type | |

### BookingRegistration

| Method | Url | Description | Sample Valid Request Body |
| ------ | --- | ----------- | ------------------------- |
| GET    | /api/me/roomTypes/{roomTypeId}/bookingRegistrations/{bookingRegistrationId} | Get the booking registration details of current user | |
| POST   | /api/me/roomTypes/{roomTypeId}/bookingRegistrations | Create new registration for current user | [JSON](#commentcreate) |
| PUT    | /api/me/roomTypes/{roomTypeId}/bookingRegistrations/{bookingRegistrationId} | update registration for current user |
| DELETE | /api/me/roomTypes/{roomTypeId}/bookingRegistrations/{bookingRegistrationId} | Delete registration for current user | |



Test them using postman or use swagger to test..

## Sample Valid JSON Request Bodys

##### Sign Up -> /api/auth/sign-up
```json
{
  "email": "string",
  "password": "string",
  "username": "string"
}
```

##### Log In -> /api/auth/login
```json
{
  "password": "string",
  "username": "string"
}
```


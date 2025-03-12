The School Management API is a RESTful service built using Node.js, Express.js, and MySQL. It allows users to:

Add new schools with name, address, latitude, and longitude.

Retrieve a sorted list of schools based on proximity to a user-provided location.

Technologies Used

Node.js (Express.js framework)

MySQL (Relational database for storing school data)

//Postman (API testing and documentation)

//Database Setup

// Create Schools Table

Run the following SQL query to create the required table:
CREATE TABLE schools (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    address VARCHAR(255) NOT NULL,
    latitude FLOAT NOT NULL,
    longitude FLOAT NOT NULL
);
API Endpoints

//Add School API
Post:http://localhost:5000/api/addSchool
Request Body (JSON):
{
    "name": "Greenwood High School",
    "address": "123 Elm Street, NY",
    "latitude": 40.7128,
    "longitude": -74.0060
}
//get schools
get:http://localhost:5000/api/schools?latitude=40.7128&longitude=-74.006
.env
DB_HOST=your_db_host
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_db_name
DB_PORT=3306
//Run the server:
npm install
node server.js

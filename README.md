# Interview-Creation-Management System By Rishabh Sharma

To run this project you have to install NodeJS (npm) and MySQL server on your machine.

To setup the web server:

Go to the project directory and run the terminal command as follows:
```
cd server
npm install
```
To setup the MySQL database:

1. Create a Database/Schema name as "InterviewDB" or run the following SQL queries.
```
CREATE DATABASE InterviewDB;
```
```
USE InterviewDB;
```
2. Add two tables "users", to hold data of the available users and "interviews", to hold the data of the upcoming interviews. Run the following SQL query.
  ```
  CREATE TABLE users (
    name VARCHAR(100) NOT NULL,
    email_id VARCHAR(100) NOT NULL,
    PRIMARY KEY (email_id));
  ```
Add some random names with email addresses to the users tables. Run the following SQL query.
```
INSERT INTO users (`name`, email_id) VALUES ('Rishabh', 'rishabh@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Kunal', 'kunal@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Luv', 'luv@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Vineet', 'vineet@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Chris', 'chris@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Vineet', 'vineet@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Zayn', 'zayn@gmail.com');
INSERT INTO users (`name`, email_id) VALUES ('Akash', 'akash@gmail.com');
```
Create the table interviews with fields id, email1, email2, startTime, endTime. Run the following SQL query.
```
CREATE TABLE interviews (
  id INT NOT NULL AUTO_INCREMENT,
  email1 VARCHAR(100) NOT NULL,
  email2 VARCHAR(100) NOT NULL,
  startTime DATETIME NOT NULL,
  endTime DATETIME NOT NULL,
  PRIMARY KEY (id));
```
You may or may not any data into the interviews table. The data will be added automatically when you scedule a new interview.

Change the following in ```server/dbServicejs``` if your MySQL server is setup on different port or has different credentials.


If facing issue regarding server not connecting:-
  ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';
  flush privileges;


Now when everything is setup. Run the server:
```
cd server
node run serve
```
If everything is successfull you will the see the text "app is running" and "db is connected" on your terminal.

Then open go to client and open start another server with index.html file open. 

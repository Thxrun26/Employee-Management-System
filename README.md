Employee Management System
Project Overview
The Employee Management System is a Java-based desktop application developed using Java Swing for the frontend, JDBC for database interaction, and MySQL as the backend. The system allows users to perform CRUD (Create, Read, Update, Delete) operations on employee records.

Features
Add new employees with details such as name, age, department, designation, salary, and joining date.
Update existing employee information.
View a list of all employees in a table.
Delete employee records.
User-friendly interface developed using Java Swing.
Technologies Used
Frontend: Java Swing for the graphical user interface (GUI).
Backend: Java with JDBC for database communication.
Database: MySQL for storing employee records.
Setup Instructions
Prerequisites
Java Development Kit (JDK) 8 or higher.
MySQL installed and running.
Apache Maven or a suitable IDE like IntelliJ IDEA or Eclipse.
Database Setup
Install and start MySQL.
Create a database named employee_db.
Use the following SQL script to create the Employee table:
sql
Copy code
CREATE DATABASE employee_db;

USE employee_db;

CREATE TABLE Employee (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    department VARCHAR(50),
    designation VARCHAR(50),
    salary DECIMAL(10,2),
    join_date DATE
);
Running the Application
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/Employee-Management-System.git
cd Employee-Management-System
Configure the MySQL connection in the Java code:
Modify the database connection URL, username, and password in the EmployeeDAO.java file:
java
Copy code
conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/employee_db", "your_username", "your_password");
Compile and run the application:
Use your preferred IDE (e.g., IntelliJ or Eclipse) or compile from the command line:
bash
Copy code
javac -d bin src/*.java
java -cp bin EmployeeForm
Contributing
If you'd like to contribute to this project, feel free to create a pull request or open an issue.

License
This project is licensed under the MIT License.

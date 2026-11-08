# Employee-Performance-Evaluation-System
📌 Overview

The Employee Performance Evaluation System is a Java-based application designed to simplify and streamline the process of evaluating employee performance within an organization. The system helps **manage employee information**, **assess individual performance**, **track achievements**, and **maintain evaluation records**. It aims to make performance assessments more organized, transparent, and efficient.


## 👥 Team Members & Responsibilities


| Members         | Role                           | Features |
|-----------------|--------------------------------|----------|
| Prachi Katiyar  | Admin & Employee Management    | Admin Login, Manage Employees, Add/Update/Delete Employee Records, View Employee Details |
| Akansha Rathore | Performance Evaluation         | Evaluate Employee Performance, Assign Scores, Manage Evaluation Criteria, Maintain Evaluation Records |
| Rishi Raj       | Reports & Performance Tracking | View Performance History, Track Employee Progress, Generate Performance Reports, Display Evaluation Results |

## 🛠️ Tech Stack

- **Backend:** Java Servlets+ JDBC
- **Database:** MariaDB
- **Server:** Apache Tomcat
- **Build Tool:** Maven
- **Frontend:** JSP + HTML + CSS + Bootstrap
- **IDE:** IntelliJ IDEA
- **Version Control:** Git and GitHub

## ✨ Key Features

### 1. Admin & Authentication
- Admin can securely log in to the system.
- Manage user accounts and access.
- View and manage the overall system through the admin dashboard.

### 2. Employee Management
- Add new employees to the system.
- View employee details and profiles.
- Update employee information whenever required.
- Delete employee records when necessary.
- Manage employee IDs, departments, and designations.

### 3. Performance Evaluation
- Evaluate employees based on their work and performance.
- Give ratings for productivity, teamwork, communication, punctuality, and quality of work.
- Calculate the overall performance score.
- Provide feedback based on employee performance.

### 4. Performance Tracking
- Keep records of previous employee evaluations.
- Track employee performance over time.
- Compare current and previous performance.
- Identify areas where employees need improvement.

### 5. Reports & Analytics
- Generate employee performance reports.
- View employee scores and ratings.
- Identify top-performing employees.
- Get an overview of the overall performance of employees.

## 📂 Project Structure

```text
Employee-Performance-Evaluation-System/
│
├── src/
│   └── main/
│       ├── java/
│       │   ├── controller/
│       │   │   ├── LoginServlet.java
│       │   │   ├── RegisterServlet.java
│       │   │   ├── EmployeeServlet.java
│       │   │   ├── EvaluationServlet.java
│       │   │   └── ReportServlet.java
│       │   │
│       │   ├── dao/
│       │   │   ├── EmployeeDAO.java
│       │   │   ├── UserDAO.java
│       │   │   └── EvaluationDAO.java
│       │   │
│       │   ├── model/
│       │   │   ├── Employee.java
│       │   │   ├── User.java
│       │   │   └── Evaluation.java
│       │   │
│       │   └── util/
│       │       └── DBConnection.java
│       │
│       ├── webapp/
│       │   ├── css/
│       │   ├── js/
│       │   ├── images/
│       │   │
│       │   ├── WEB-INF/
│       │   │   └── web.xml
│       │   │
│       │   ├── login.jsp
│       │   ├── register.jsp
│       │   ├── dashboard.jsp
│       │   ├── employees.jsp
│       │   ├── evaluation.jsp
│       │   └── reports.jsp
│       │
│       └── resources/
│
├── database/
│   └── schema.sql
│
├── pom.xml
├── README.md
└── .gitignore
```
🗄️ Database Information

Database Name: employee_performance_db

Database Tables:

`users`- Stores login credentials and user roles such as Admin and Employee.

`employees`- Stores employee details such as employee ID, name, email, department, and designation.

`evaluations`- Stores employee performance scores, ratings, evaluation dates, and feedback.

`performance_criteria`- Stores evaluation criteria such as productivity, teamwork, communication, and punctuality.

Prerequisites:

1. Java JDK (17 or compatible version)
2. IntelliJ IDEA
3. Apache Tomcat Server (Tomcat 9 or 10, depending on Servlet API compatibility)
4. MariaDB
5. Maven
6. Git

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

Open the terminal and run:

```bash
git clone https://github.com/your-username/Employee-Performance-Evaluation-System.git
```

Navigate to the project folder:

```bash
cd Employee-Performance-Evaluation-System
```

### Step 2: Open the Project in IntelliJ IDEA

1. Open IntelliJ IDEA.
2. Select **File → Open**.
3. Choose the cloned project folder.
4. Wait for Maven to download and configure the required dependencies.
5. Make sure the correct JDK is selected in Project Structure.

### Step 3: Configure the Database

1. Start your MariaDB server.
2. Open MariaDB using your preferred database client.
3. Create the project database:

```sql
CREATE DATABASE employee_performance_db;
```

4. Select the database:

```sql 
USE employee_performance_db;
```

5. Execute the SQL script provided in the `database` folder to create the required tables.
6. Open `DBConnection.java` and configure your database connection details:

```java
String url = "jdbc:mariadb://localhost:3306/employee_performance_db";
String username = "root";
String password = "your_password";
```

Replace the username and password with your MariaDB credentials.

### Step 4: Configure Apache Tomcat

1. Download and install Apache Tomcat.
2. Open IntelliJ IDEA.
3. Configure Tomcat through the Smart Tomcat plugin or your available application server configuration.
4. Set the Tomcat installation directory.
5. Select the project and configure its web application context path.
6. Make sure the application is configured to run on the correct port (default: 8080).

### Step 5: Build the Project

Open the IntelliJ terminal and execute:

```bash
mvn clean install
```

This command cleans the previous build, downloads required dependencies, and builds the project.

### Step 6: Run the Application

1. Start the MariaDB server.
2. Start the Apache Tomcat server using IntelliJ IDEA.
3. Wait for the application to deploy successfully.
4. Open your browser and visit:

```text
http://localhost:8080/Employee-Performance-Evaluation-System/
```

5. The application login page should appear.

### Step 7: Login to the Application

- Open the login page.
- Enter your registered email and password.
- Access the dashboard according to your assigned role.
- Start managing employees and their performance evaluations.

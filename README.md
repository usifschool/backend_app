User Authentication and Management System
This is a Spring Boot application that provides user authentication and management features, including:

User registration

User login

Password reset functionality

Secure access to the home page

The application uses Spring Security for authentication, Thymeleaf for the frontend, and MariaDB for database storage.

Features
User Registration:

Users can register by providing their email, password, and full name.

Passwords are securely hashed using BCryptPasswordEncoder.

User Login:

Users can log in using their registered email and password.

Unauthenticated users are redirected to the login page when trying to access protected routes.

Password Reset:

Users can reset their password by providing their email, old password, and new password.

Home Page:

Authenticated users can access the home page.

The home page includes a Logout button and a Reset Password button.

Logout:

Users can log out, which invalidates their session and redirects them to the login page.

Technologies Used
Backend:

Spring Boot

Spring Security

Spring Data JPA

MariaDB (via XAMPP)

Frontend:

Thymeleaf

Bootstrap (for styling)

Tools:

Maven (for dependency management)

IntelliJ IDEA (or any IDE of your choice)

Setup Instructions
Prerequisites
Java Development Kit (JDK):

Install JDK 23 or later.

Set the JAVA_HOME environment variable.

XAMPP:

Install XAMPP and start the Apache and MySQL services.

MariaDB:

Create a database named user_auth in phpMyAdmin.

IDE:

Install IntelliJ IDEA, Eclipse, or any IDE of your choice.

Steps to Run the Project
Clone the Repository
Configure the Database:

Update the application.properties_copy file into application.properties with your MariaDB credentials:


Run the Application:

Open the project in your IDE.

Run the UserAuthApplication class (or use the command mvn spring-boot:run).

Access the Application:

Open your browser and go to http://localhost:8080.

Use the following endpoints:

Register: http://localhost:8080/register

Login: http://localhost:8080/login

Reset Password: http://localhost:8080/reset-password

Home: http://localhost:8080/home (requires login)

Project Structure
Copy
src/main/java
├── com.example.userauth
│   ├── config
│   │   └── SecurityConfig.java          # Spring Security configuration
│   ├── controller
│   │   ├── HomeController.java          # Handles home page requests
│   │   ├── LoginController.java         # Handles login page requests
│   │   └── UserController.java          # Handles user registration and password reset
│   ├── entity
│   │   └── User.java                    # User entity class
│   ├── repository
│   │   └── UserRepository.java          # User repository for database operations
│   ├── service
│   │   └── UserService.java             # Business logic for user operations
│   └── UserAuthApplication.java         # Main application class
src/main/resources
├── static                               # Static resources (CSS, JS, etc.)
├── templates                            # Thymeleaf templates
│   ├── home.html                        # Home page template
│   ├── login.html                       # Login page template
│   ├── register.html                    # Registration page template
│   └── reset-password.html              # Reset password page template
└── application.properties               # Application configuration

License
This project is licensed under the MIT License. See the LICENSE file for details.
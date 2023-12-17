** Blogging System

This project is a web application that empowers users to create and manage their blogs online. It leverages Spring Boot, Spring MVC, Spring Security, Hibernate, MySQL, Thymeleaf,

**Features

User registration and login with email verification and password reset
User profile management with avatar upload and editing capabilities
Intuitive blog creation and editing interface with support for rich text, images, and multimedia content
Blog categorization and filtering based on tags, categories, and publication dates
Seamless integration with social media platforms for sharing blog posts
Commenting system for readers to engage with blog content
Administrator dashboard with comprehensive CRUD operations for blogs, users, and comments
Analytics and reports on blog traffic, user engagement, and popular conten

**Installation
To run this project, ensure that you have Java 8, Maven, and MySQL installed on your system.
- Clone this repository:

**bash
git clone https://github.com/frank/Blogging system.git
cd Blogging system

- Edit the application.properties file in the src/main/resources folder and change the following properties according to your MySQL configuration:

**properties

server.port=8080
spring.datasource.url=jdbc:mysql://localhost:3306/spring?createDatabaseIfNotExist=true
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=root
 spring.datasource.password=
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.generate-ddl=true
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect //latest version
**Email Configuration

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=tuyishimewillyfrank@gmail.com
spring.mail.password=smaoaozfjlbrewui
spring.mail.properties.mail.smtp.starttls.enable=true
spring.mail.properties.mail.smtp.starttls.required=true
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.connectiontimeout=5000
spring.mail.properties.mail.smtp.timeout=5000
spring.mail.properties.mail.smtp.writetimeout=5000
spring.servlet.multipart.max-file-size = 5MB
spring.servlet.multipart.max-request-size = 5MB


*Run the project using Maven:

**bash
mvn spring-boot:run


- Open http://localhost:8080 in your browser and enjoy the application.

 **Screenshots
 
**Source Code:
The source code for the Blogging System project can be found in the blog repository.Here are the key directories and files:

1. **src/main/java:** Contains the Java source code for the project.
   **com.example.blog: Main package for the application.
   **controller: Contains controllers handling web requests.
   **model: Defines the data models used in the application.
   **repository: Provides interfaces for database access.
   **service: Implements business logic and interacts with repositories.
   **security:Manages security configurations.
   **BloggingSystemApplication.java: Main class to run the Spring Boot application.

2. **src/main/resources: Contains configuration files and static resources.
  **application.properties: Configuration file for database, mail, and other properties.
  **templates: Thymeleaf HTML templates for web pages.

3. **pom.xml:  Maven Project Object Model file specifying dependencies and build configurations.

4. **src/main/sql:  Contains SQL script for initializing the database (`blogging_system.sql`).

5. **Other files:** There may be additional configuration files, scripts, or assets required for the project.

**Database Schema:
  
  *Database Tables:
User Table:

Columns: id, account_non_locked,created_date,password,pdate_date, username,
Blog Table:

Columns: id,created date, deleted,description,image,title,update_date, user_id
Relationships: Many-to-One with User (user_id)
Comment Table:

Columns: id, content, comment_author, comment_date, blog_id,
Relationships: Many-to-One with Blog (blog_id), Many-to-One with User (user_id)
Relationships:
User-to-Blog: One-to-Many
Blog-to-Comment: One-to-Many

**User Documentation:
 
 *How to Use the Application:
User Registration:

Open the application and click on the "Register" button.
Fill in the required details and submit the form.
Verify your email and log in.
Creating a Blog:

After logging in, navigate to the "Create Blog" section.
Enter the title and content of your blog.
Optionally, add tags or select categories.
Click on the "Submit" button.

**Social Media Integration:

To share a blog post, click on the social media icons provided.
Authorize the application to post on your behalf.
Commenting:

*Readers can leave comments on blog posts.
Enter the comment in the provided section and submit.
Administrator Dashboard:

*Log in with administrator credentials.
Access the dashboard to manage blogs, users, and comments.

**Technical Documentation:
Architecture:
The application follows the Model-View-Controller (MVC) architecture.
Spring Boot is used as the backend framework, providing RESTful endpoints.
Thymeleaf is employed for server-side templating, rendering views.
Hibernate is used for data persistence, with MySQL as the relational database.

**Implementation Details:
User authentication is handled using Spring Security.
Social media integration is achieved through OAuth.
Frontend design is enhanced using Bootstrap for a responsive and visually appealing interface.

**Technologies Used:
Java 8
Spring Boot, Spring MVC, Spring Security
Hibernate
MySQL
Thymeleaf
Bootstrap
**Additional Considerations:
The project adheres to best practices in terms of security, data integrity, and code maintainability.



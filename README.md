NImap-task1) How did you run the code?
Step 1: Open the Project in Eclipse Open Eclipse IDE → File → Import → Maven → Existing Maven Projects Select your project folder and click Finish
Step 2: Configure PostgreSQL Database Ensure PostgreSQL is running. Update application.properties: properties spring.datasource.url=jdbc:postgresql://localhost:5432/yourdbname spring.datasource.username=yourusername spring.datasource.password=yourpassword spring.jpa.hibernate.ddl-auto=update Step 3: Run the Application Right-click the main class (@SpringBootApplication) → Run As → Spring Boot App The application starts at http://localhost:8080/
How did you run the machine test? Step 1: API Testing using Postman GET all categories:
GET http://localhost:8080/api/categories?page=1 POST a new category:

POST http://localhost:8080/api/categories Content-Type: application/json

{ "name": "Employee" } Similarly, test for Product APIs.
Step 2: Verify Database Entries Open pgAdmin Run queries:

SELECT * FROM categories; SELECT * FROM products;
DB Design One Category → Many Products

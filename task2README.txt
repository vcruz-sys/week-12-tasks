1. Create an Entity-Relationship Diagram (ERD) showing entities, attributes, and relationships.

You may:
Hand-draw the ERD, and take a clear photo of the drawing.
OR use a digital tool (e.g., Figma, Canva, draw.io), and take a screenshot.

2. Save the image and place it in a “Task2” folder.

3. SQL Schema

Write CREATE TABLE statements for at least three entities, including:
- Primary keys (PK)
- Foreign keys (FK)
- Appropriate data types and NOT NULL constraints.

Please add your SQL query below AND add an explanation: 

(copy and paste SQL Query here)
CREATE TABLE Company (
    company_id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    location VARCHAR(100) NOT NULL
);

CREATE TABLE Employee (
    employee_id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    role VARCHAR(50) NOT NULL,
    company_id INT NOT NULL,
    FOREIGN KEY (company_id) REFERENCES Company(company_id)
);

CREATE TABLE Product (
    product_id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    price DECIMAL(10,2) NOT NULL,
    company_id INT NOT NULL,
    FOREIGN KEY (company_id) REFERENCES Company(company_id)
);

(add an explanation of your query here)
The Company table stores company details. company_id is the primary key to uniquely identify each company.
The Employee table stores employee information. employee_id is the primary key, and company_id is a foreign key linking employees to their company (one-to-many relationship).
The Product table stores product details. product_id is the primary key, and company_id is a foreign key linking products to the company that sells them.


4. Save this file in a "Task2" folder along with your ERD diagram

5. For submission, commit and push your "Task2" folder with the two files to your GitHub.


# sql-challenge
Module 9
Employee Database 

Overview

This project consists of an Employee Database schema with six tables: Employees, Titles, Salaries, Departments, Dept_Employees, and Dept_Managers. The tables are designed to store and manage employee-related data efficiently.

Entity Relationship Diagram (ERD)

Below are the questions explored and answered using the queries created within the Queries.sql file:


Data Analysis

1. List the employee number, last name, first name, sex, and salary of each employee.

2. List the first name, last name, and hire date for the employees who were hired in 1986.

3. List the manager of each department along with their department number, department name, employee number, last name, and first name.

4. List the department number for each employee along with that employee’s employee number, last name, first name, and department name.

5. List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.

6. List each employee in the Sales department, including their employee number, last name, and first name.

7. List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.

8. List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).

SQL Query Examples:

Get Employees in Sales Department

SELECT e.emp_no, e.last_name, e.first_name
FROM employees e
INNER JOIN dept_emp de 
ON e.emp_no = de.emp_no
INNER JOIN departments d 
ON de.dept_no = d.dept_no
WHERE d.dept_name = 'Sales';

Count Employees by Last Name

SELECT last_name, COUNT(*) AS name_count
FROM employees
GROUP BY last_name
ORDER BY name_count DESC;

Usage

Run the provided SQL scripts within the EmployeeSQL  folder to create the schema.

Populate the tables with the csv data within the data folder.

Use the queries within the Queries.sql file to extract meaningful insights from the data.

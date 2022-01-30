<h3>HR Database Exercises</h3>

<h8>#1. Write a query to display the names (first_name, last_name) using alias name “First Name", "Last Name"

ANS: SELECT employees.FirstName,employees.LastName FROM employees


#2. Write a query to get unique department ID from employee TABLE
ANS: SELECT DISTINCT department ID FROM employee 

 
#3. Write a query to get all employee details from the employee table order by first name, descending
ANS: SELECT * FROM employee ORDER BY FIRST NAME DESC;

#4. Write a query to get the names (first_name, last_name), salary, PF of all the employees (PF is #calculated as 15% of salary)
ANS: 
SELECT employees.first_name,employees.last_name ,round(employees.salary,2) AS salary , round(employees.salary*15,2) AS PF FROM employees

#5. Write a query to get the employee ID, names (first_name, last_name), salary in ascending order of #salary.
ANS:
SELECT employees.first_name,employees.last_name ,round(employees.salary,2) AS Salary FROM employees ORDER BY employees.salary

#6. Write a query to get the total salaries payable to employees
ANS: SELECT SUM(salary) FROM employees

#7. Write a query to get the maximum and minimum salary from employees table
ANS: SELECT MAX(salary),MIN(salary) FROM employees
 
#8. Write a query to get the average salary and number of employees in the employees table
ANS: SELECT AVG(salary),COUNT(employee_id)  FROM employees
 
#9. Write a query to get the number of employees working with the company
ANS: SELECT COUNT(employee_id) AS TotalNumberofEmployees  FROM employees
 
#10. Write a query to get the number of jobs available in the employees table
ANS: SELECT DISTINCT count(job_id) FROM employees
 
#11. Write a query get all first name from employees table in upper case
ANS: SELECT upper(first_name) FROM employees

 
#12. Write a query to get the first 3 characters of first name from employees table.

ANS: SELECT substring(first_name,1,3) AS Trimname FROM employees

#13. Write a query to get first name from employees table after removing white spaces from both side

ANS: SELECT TRIM(first_name) FROM employees

#14. Write a query to get the length of the employee names (first_name, last_name) from employees table.

ANS: SELECT length(first_name) AS LenOfFname,length(last_name) AS LenofLastName FROM employees

#15. Write a query to check if the first_name fields of the employees table contains numbers
ANS: SELECT first_name FROM employees WHERE  first_name REGEXP  '[0-9]'
 
#16. Write a query to display the name (first_name, last_name) and salary for all employees whose salary is #not in the range $10,000 through $15,000
ANS: SELECT first_name, last_name, salary FROM employees WHERE salary not BETWEEN 10000 AND 15000
 

#17. Write a query to display the name (first_name, last_name) and department ID of all employees in #departments 30 or 100 in ascending order
ANS: SELECT first_name, last_name,department_id FROM employees  WHERE department_id=30 OR department_id=100 order BY department_id;


#18. Write a query to display the name (first_name, last_name) and salary for all employees whose salary is not in the range $10,000 through $15,000 and are in department 30 or 100
ANS: SELECT first_name, last_name, salary,department_id FROM employees WHERE salary not BETWEEN 10000 AND 15000 and department_id=30 OR department_id=100 

 




#19. Write a query to display the name (first_name, last_name) and hire date for all employees who were hired in 1987
ANS: SELECT first_name, last_name,hire_date FROM employees WHERE hire_date  LIKE '1987%%'


 




#20. Write a query to display the first_name of all employees who have both "b" and "c" in their first name

ANS: SELECT first_name FROM employees WHERE first_name LIKE '%b%'
and first_name LIKE '%c%';

 

#21. Write a query to display the last name, job, and salary for all employees whose job is that of a Programmer or a Shipping Clerk, and whose salary is not equal to $4,500, $10,000, or $15,000
ANS: SELECT last_name, job_id, salary FROM employees  WHERE  job_id='IT_PROG' OR job_id='SH_CLERK' and salary not like 4,500 or 10,000 or 15,000.


 
#22. Write a query to display the last name of employees whose names have exactly 6 characters 
ANS: SELECT last_name,length(last_name) AS LengthOLName  FROM employees WHERE LENGTH(last_name )=6



 

#23. Write a query to display the last name of employees having 'e' as the third character
ANS: SELECT last_name  FROM employees WHERE last_name LIKE '__e%'
 

#24. Write a query to get the job_id and related employee's id FI_ACCOUNT 110 ,113 ,111 ,109 ,112.
ANS: SELECT job_id,employee_id FROM employees  order BY job_id

 









#25. Write a query to update the portion of the phone_number in the employees table, within the phone number the substring '124' will be replaced by '999'
Ans: update employees 
SET phone_number = REPLACE(phone_number, '124', '999') 
WHERE phone_number LIKE '%124%'

 
#26. Write a query to get the details of the employees where the length of the first name greater than or equal to 8
ANS: SELECT * FROM employees  WHERE length(first_name)>=8
 
27. Write a query to append '@example.com' to email field

 












28. Write a query to extract the last 4 character of phone numbers

ANS: SELECT right(phone_number,4) FROM employees

 





29. Write a query to get the last word of the street address.
Ans: SELECT SUBSTRING_INDEX(street_address, ' ', -1) as trimaddress from locations;

 










30. Write a query to get the locations that have minimum street length
ANS: SELECT street_address FROM locations ORDER by length(street_address) LIMIT 1;

 
31. Write a query to display the first word from those job titles which contains more than one words
Ans. Select job_titles substr(job_title,1,instr(job_title,” ”)-1)




32. Write a query to display the length of first name for employees where last name contain character 'c' after 2nd position.

ANS: SELECT first_name, last_name FROM employees WHERE INSTR(last_name,'C') > 2;

 






33. Write a query that displays the first name and the length of the first name for all employees whose name starts with the letters 'A', 'J' or 'M'. Give each column an appropriate label. Sort the results by the employees' first names.
ANS: SELECT first_name "Name",LENGTH(first_name) "Length"FROM employees
WHERE first_name LIKE 'J%' OR first_name LIKE 'M%' OR first_name LIKE 'A%'
ORDER BY first_name ;

 



34. Write a query to display the first name and salary for all employees. Format the salary to be 10 characters long, left-padded with the $ symbol. Label the column SALARY
ANS: SELECT first_name,LPAD(salary, 10, '$') SALARY FROM employees;</h8>


 


# Joins in Postgre SQL

Join is used to combine data or rows from one or more tables based on a common field between them. These common fields are generally the Primary key of the first table and Foreign key of other tables.

There are 4 types of joins in PostgreSQL:

1.Inner Join

2.Left Join

3.Right Join

4.Full Outer Join

5.Cross Join

INNER JOIN:-

JOIN (or explicitly INNER JOIN ) returns rows that have matching values in both
tables.


Here is an employee table

![employee table](./images/employee-table-inner-and-left-join.png)

Here is the department table
![department table](./images/department-table-inner-and-left-join.png)


Example:

```
SELECT employee.Firstname, department.dept_name
FROM employee
INNER JOIN department
ON employee.emp_id = department.emp_id;
```

![innerjoin](./images/inner-join.png)



LEFT JOIN:-

LEFT JOIN returns all rows from the left table with corresponding rows from the right
table. If there's no matching row, NULL s are returned as values from the second
table.



Example:-

```
select employee.FirstName , department.dept_name
from employee
left join department
on employee.emp_id=department.emp_id;
```

![leftjoin](./images/left-join.png)

RIGHT JOIN:-

RIGHT JOIN returns all rows from the right table with corresponding rows from the
left table. If there's no matching row, NULL s are returned as values from the left
table.







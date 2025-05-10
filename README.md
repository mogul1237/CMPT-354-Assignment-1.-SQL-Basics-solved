# CMPT-354-Assignment-1.-SQL-Basics-solved

Download Here: [CMPT 354 Assignment 1. SQL Basics solved](https://jarviscodinghub.com/assignment/assignment-1-sql-basics-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Objectives

In this assignment, you will go through the pipeline of using SQL to store and query a database. You will learn the followings:

How to create a table
How to insert data into a table
How to select certain rows or columns from a table
How to join two tables together
How to use expressions

In addition, you will get familiar with Jupyter (a widely-used tool in the data science world).

We will choose SQLite as our DBMS. In contrast to many other database management systems (e.g., Oracle, DB2, and SQL Servier), SQLite is not a client–server database engine. Rather, it is embedded into the end program. This unique feature has led it to be adopted by billions of applications.

Setup & Warmup

Please follow this setup page to setup environment
Please download the warmup.ipynb notebook. It will help you get familiar with SQLite and Jupyter notebook. If you have any question, please ask on Piazza.

Task 1. Using SQL to create a database (9 points)

In this task, your goal is to create a database (named coursys), and then create two tables in the database. The first table is named students and the second table is named grades.

Please execute the following cell to load the ipython-sql extension.
In [ ]:
%load_ext sql

1.1 (1 point) Create an empty database named coursys
In [ ]:
#REPLACE WITH YOUR CODE#

1.2 (4 points) Create a table named grades

The grades table has four columns and six rows as shown below.

studentid, course, mark, credit
1, CMPT 354, 90, 3.5
1, MATH 251, 85, 4
1, CMPT 120, 79.5, 5
2, CMPT 354, 95, 3.5
2, CMPT 120, 59, 5
2, MATH 251, 70, 4
Please write an SQL query to create the grades table. Note that the table has to meet the following requirements.

studentid – integer
course – char(10)
mark and credit – double
(studentid, course) is Primary Key
studentid references students.id
In [ ]:
#REPLACE WITH YOUR CODE#

Please write SQL queries to insert the above data (six rows) into the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

1.3 (4 points) Create a table named students

The students table has four columns and two rows as shown below.

id, name, gender, age
1, Justin Bieber, Male, 18
2, Celine Dion, Female, 19
Please write an SQL query to create the students table. Note that the table has to meet the following requirements.

id, age – integer
name – varchar(30)
gender – char(6)
id is Primary Key
name cannot be NULL
In [ ]:
#REPLACE WITH YOUR CODE#

Please write SQL queries to insert the above data (2 rows) into the student table
In [ ]:
#REPLACE WITH YOUR CODE#

Task 2. Using SQL to query a database (11 points)

2.1 (1 point) Please write an SQL query to show all rows in the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

2.2 (1 point) Please write an SQL query to show the rows whose course is “CMPT 354” in the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

2.3 (1 point) Please write an SQL query to show the rows whose mark is larger than 60 and credit is no smaller than 4 in the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

2.4 (1 point) Please write an SQL query to show the rows whose course starts with “CMPT” in the grades table.
In [ ]:
#REPLACE WITH YOUR CODE#

2.5 (1 point) Please write an SQL query to show studentid, course and mark of all rows in the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

2.6 (1 point) Please write an SQL query to show distinct course of all rows in the grades table
In [ ]:
#REPLACE WITH YOUR CODE#

2.7 (1 point) Please write an SQL query to show studentid, course and markpoint of all rows in the grades table. markpoint is defined as markpoint= mark * credit.
In [ ]:
#REPLACE WITH YOUR CODE#

2.8 (2 points) Please write an SQL query to find the students who have taken “CMPT 354” and show their name, mark.
In [ ]:
#REPLACE WITH YOUR CODE#

2.9 (2 point) Please write an SQL query to compute lettergrade of each row in the grades table, and show studentid, course and lettergrade of all rows in the grades table. lettergrade is computed as follows:

If mark >= 90, then lettergrade = “A”
If 80 <= mark < 90, then lettergrade = “B”
If 70 <= mark < 80, then lettergrade = “C”
If 60 <= mark < 70, then lettergrade = “D”
If mark < 60, then lettergrade = “F”
Hint: please use a CASE expression to transform numerical marks to letters.
In [ ]:
#REPLACE WITH YOUR CODE#

Submission

Complete the code in this notebook A1.ipynb, and submit it to the CourSys activity Assignment 1.

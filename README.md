# Internship_Project_for_SQL_Developer
# Code for Library database and two tables Author and Books by using MySQL.

CREATE DATABASE LibraryDB;
USE LibraryDB;

CREATE TABLE Author(
Author_id INT PRIMARY KEY,
first_name VARCHAR(50),
last_name VARCHAR(50)
);

INSERT INTO Author Values
(101, 'William', 'Shakespeare'),
(102, 'Rabindranath', 'Tagore'),
(103, 'Hariwanshrai', 'Bachchan');

SELECT * FROM Author;

CREATE TABLE Books(
Book_id INT PRIMARY KEY,
Title VARCHAR(100),
published_year DATE,
Author_id INT NOT NULL,
FOREIGN KEY(Author_id) REFERENCES Author(Author_id)
);

INSERT INTO Books Values
(1, 'Romeo And Juliet', '1597-01-01', 101),
(2, 'Gitanjali', '1910-01-01', 102),
(3, 'Madhushala', '1935-01-01', 103);

SELECT * FROM Books;

SELECT * FROM Author
JOIN Books
ON Author.Author_id = Books.Author_id;   


# Identifying Entities and relationships by ER Diagram
<img width="1332" height="760" alt="image" src="https://github.com/user-attachments/assets/891a4a5f-8611-406f-b7a7-70050efd73aa" />


# Tes-Dumbways-SQL
cuma bisa ngerjain setengah soal nomor 4



4.

Microsoft Windows [Version 10.0.17134.1304]
(c) 2018 Microsoft Corporation. All rights reserved.

C:\Users\Hp>cd /d F:

F:\>"Program Files (x86)/XAMPP/mysql/bin/mysql.exe" -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 11
Server version: 10.4.17-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databses;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'databses' at line 1
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
+--------------------+
5 rows in set (0.001 sec)

MariaDB [(none)]> create database school;
Query OK, 1 row affected (0.002 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| school             |
| test               |
+--------------------+
6 rows in set (0.001 sec)

MariaDB [(none)]> use school
Database changed
MariaDB [school]> create table school_tb (Id int, NPSN varchar(8), name_school varchar(25), address text, logo_school blob, school_level varchar (10), status_school varchar (10), user_id varchar (10), primary key (id));
Query OK, 0 rows affected (0.764 sec)

MariaDB [school]> show tables;
+------------------+
| Tables_in_school |
+------------------+
| school_tb        |
+------------------+
1 row in set (0.093 sec)

MariaDB [school]> desc school_tb;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| Id            | int(11)     | NO   | PRI | NULL    |       |
| NPSN          | varchar(8)  | YES  |     | NULL    |       |
| name_school   | varchar(25) | YES  |     | NULL    |       |
| address       | text        | YES  |     | NULL    |       |
| logo_school   | blob        | YES  |     | NULL    |       |
| school_level  | varchar(10) | YES  |     | NULL    |       |
| status_school | varchar(10) | YES  |     | NULL    |       |
| user_id       | varchar(10) | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
8 rows in set (0.197 sec)



~~~~~~~~~
Soal 4.

A.

F:\>"Program Files (x86)/XAMPP/mysql/bin/mysql.exe" -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 16
Server version: 10.4.17-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
+--------------------+
5 rows in set (0.001 sec)

MariaDB [(none)]> create database school;
Query OK, 1 row affected (0.002 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| school             |
| test               |
+--------------------+
6 rows in set (0.001 sec)

MariaDB [(none)]> use school
Database changed
MariaDB [school]> create table school_tb (Id int, NPSN varchar(8), name_school varchar(25), address text, logo_school blob, school_level varchar (10), status_school varchar (10), user_id varchar (10), primary key (id));
Query OK, 0 rows affected (0.764 sec)

MariaDB [school]> show tables;
+------------------+
| Tables_in_school |
+------------------+
| school_tb        |
+------------------+
1 row in set (0.093 sec)

MariaDB [school]> desc school_tb;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| Id            | int(11)     | NO   | PRI | NULL    |       |
| NPSN          | varchar(8)  | YES  |     | NULL    |       |
| name_school   | varchar(25) | YES  |     | NULL    |       |
| address       | text        | YES  |     | NULL    |       |
| logo_school   | blob        | YES  |     | NULL    |       |
| school_level  | varchar(10) | YES  |     | NULL    |       |
| status_school | varchar(10) | YES  |     | NULL    |       |
| user_id       | varchar(10) | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
8 rows in set (0.197 sec)

MariaDB [school]> insert into school_tb (id, NPSN, name_school, address, logo_school, school_level, status_school, user_id)
    -> values
    -> ( 1, "1111", "SMP Trajan", "Rylai Palace", '-', "Semester 5", "Swasta", "9999"),
    -> ( 2, "2222", "SMP Warlord", "Axe Palace", '-', "Semester 8", "Swasta", "8888");
ERROR 1062 (23000): Duplicate entry '1' for key 'PRIMARY'
MariaDB [school]> insert into school_tb (id, NPSN, name_school, address, logo_school, school_level, status_school, user_id)
    -> values
    -> ( 1, "1111", "SMP Trajan", "Rylai Palace", '-', "Semester 5", "Swasta", "9999");
ERROR 1062 (23000): Duplicate entry '1' for key 'PRIMARY'
MariaDB [school]> drop table 'school_tb';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near ''school_tb'' at line 1
MariaDB [school]> drop table school_tb;
Query OK, 0 rows affected (0.327 sec)

MariaDB [school]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| school             |
| test               |
+--------------------+
6 rows in set (0.001 sec)

MariaDB [school]> create table school_tb (Id int, NPSN varchar(8), name_school varchar(25), address text, logo_school blob, school_level varchar (10), status_school varchar (10), user_id varchar (10), primary key (Id));
Query OK, 0 rows affected (0.237 sec)

MariaDB [school]> show tables;
+------------------+
| Tables_in_school |
+------------------+
| school_tb        |
+------------------+
1 row in set (0.001 sec)

MariaDB [school]> desc school_tb;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| Id            | int(11)     | NO   | PRI | NULL    |       |
| NPSN          | varchar(8)  | YES  |     | NULL    |       |
| name_school   | varchar(25) | YES  |     | NULL    |       |
| address       | text        | YES  |     | NULL    |       |
| logo_school   | blob        | YES  |     | NULL    |       |
| school_level  | varchar(10) | YES  |     | NULL    |       |
| status_school | varchar(10) | YES  |     | NULL    |       |
| user_id       | varchar(10) | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
8 rows in set (0.011 sec)

MariaDB [school]> insert into school_tb (id, NPSN, name_school, address, logo_school, school_level, status_school, user_id)
    -> values
    -> ( 1, "1111", "SMP Trajan", "Rylai Palace", '-', "Semester 5", "Swasta", "9999");
Query OK, 1 row affected (0.134 sec)

MariaDB [school]> select * from school_tb;
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
| Id | NPSN | name_school | address      | logo_school | school_level | status_school | user_id |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
|  1 | 1111 | SMP Trajan  | Rylai Palace | -           | Semester 5   | Swasta        | 9999    |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
1 row in set (0.045 sec)

MariaDB [school]> insert into school_tb (id, NPSN, name_school, address, logo_school, school_level, status_school, user_id)
    -> values
    -> ( 2, "2222", "SMP Warlord", "Axe Palace", '-', "Semester 8", "Swasta", "8888");
Query OK, 1 row affected (0.132 sec)

MariaDB [school]> select * from school_tb;
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
| Id | NPSN | name_school | address      | logo_school | school_level | status_school | user_id |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
|  1 | 1111 | SMP Trajan  | Rylai Palace | -           | Semester 5   | Swasta        | 9999    |
|  2 | 2222 | SMP Warlord | Axe Palace   | -           | Semester 8   | Swasta        | 8888    |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
2 rows in set (0.001 sec)

MariaDB [school]> update school_tb set name_school ="SMP Trajan" where name_school = "SMP Sparta";
Query OK, 0 rows affected (0.188 sec)
Rows matched: 0  Changed: 0  Warnings: 0

MariaDB [school]> select * from school_tb;
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
| Id | NPSN | name_school | address      | logo_school | school_level | status_school | user_id |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
|  1 | 1111 | SMP Sparta  | Rylai Palace | -           | Semester 5   | Swasta        | 9999    |
|  2 | 2222 | SMP Warlord | Axe Palace   | -           | Semester 8   | Swasta        | 8888    |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+
2 rows in set (0.001 sec)


MariaDB [school]> create table user(
    -> id int not null auto_increment primary key,
    -> name varchar(20),
    -> email varchar (20),
    -> constraint id foreign key (id) references school_tb (Id));
Query OK, 0 rows affected (0.300 sec)

MariaDB [school]> show tables;
+------------------+
| Tables_in_school |
+------------------+
| school_tb        |
| user             |
+------------------+
2 rows in set (0.001 sec)

MariaDB [school]> desc user;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| name  | varchar(20) | YES  |     | NULL    |                |
| email | varchar(20) | YES  |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
3 rows in set (0.082 sec)

MariaDB [school]> insert into user values ("1","Esmeralda","esme@gmail.com"),("2","Archon","arcwarden@gmail.com");
Query OK, 2 rows affected (0.220 sec)
Records: 2  Duplicates: 0  Warnings: 0

MariaDB [school]> select * from user;
+----+-----------+---------------------+
| id | name      | email               |
+----+-----------+---------------------+
|  1 | Esmeralda | esme@gmail.com      |
|  2 | Archon    | arcwarden@gmail.com |
+----+-----------+---------------------+
2 rows in set (0.001 sec)

MariaDB [school]> show tables;
+------------------+
| Tables_in_school |
+------------------+
| school_tb        |
| user             |
+------------------+
2 rows in set (0.001 sec)

MariaDB [school]> desc user;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| name  | varchar(20) | YES  |     | NULL    |                |
| email | varchar(20) | YES  |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
3 rows in set (0.010 sec)

MariaDB [school]> desc school_tb;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| Id            | int(11)     | NO   | PRI | NULL    |       |
| NPSN          | varchar(8)  | YES  |     | NULL    |       |
| name_school   | varchar(25) | YES  |     | NULL    |       |
| address       | text        | YES  |     | NULL    |       |
| logo_school   | blob        | YES  |     | NULL    |       |
| school_level  | varchar(10) | YES  |     | NULL    |       |
| status_school | varchar(10) | YES  |     | NULL    |       |
| user_id       | varchar(10) | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
8 rows in set (0.068 sec)

MariaDB [school]> select * from school_tb inner join user on school_tb.Id = user.id;
+----+------+-------------+--------------+-------------+--------------+---------------+---------+----+-----------+---------------------+
| Id | NPSN | name_school | address      | logo_school | school_level | status_school | user_id | id | name      | email               |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+----+-----------+---------------------+
|  1 | 1111 | SMP Sparta  | Rylai Palace | -           | Semester 5   | Swasta        | 9999    |  1 | Esmeralda | esme@gmail.com      |
|  2 | 2222 | SMP Warlord | Axe Palace   | -           | Semester 8   | Swasta        | 8888    |  2 | Archon    | arcwarden@gmail.com |
+----+------+-------------+--------------+-------------+--------------+---------------+---------+----+-----------+---------------------+
2 rows in set (0.213 sec)


# Steps to run this project:

### 1)First setup you mysql database

#### a)Open my sql using "mysql -u root -p" 
#### b)Create database and initialise data in using following commands:-
CREATE DATABASE IF NOT EXISTS `mydb` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `mydb`;

CREATE TABLE IF NOT EXISTS `accounts` (
  `id` int(11) NOT NULL,
  `username` varchar(50) NOT NULL,
  `password` varchar(255) NOT NULL,
  `email` varchar(100) NOT NULL
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

INSERT INTO `accounts` (`id`, `username`, `password`, `email`) VALUES (1, 'test', 'test', 'test@test.com');

ALTER TABLE `accounts` ADD PRIMARY KEY (`id`);
ALTER TABLE `accounts` MODIFY `id` int(11) NOT NULL AUTO_INCREMENT,AUTO_INCREMENT=2;

#### (Default username and password is "test" and "test")


### 2)Input your database credentials in *database.js.*
#### (Database credentials refer to username and password of mysql and name od databse in mysql.)


var connection = mysql.createConnection({

    host     : 'localhost',
    user     : 'nikolai',
    password : 'node',
    database : 'mydb'
    
});

### 3)Open your terminal and write 'npm install' to install required *nodejs* packages


### 4)Finally 'node server' to start the server of the project.




####  Live website link-  [Click here](http://ec2-3-93-17-4.compute-1.amazonaws.com:3000)

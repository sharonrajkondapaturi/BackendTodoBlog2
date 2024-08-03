### Let's start with Node js

----> Todo Backend

----> in this project i used NODE.js for backend development

----> used libraries are 
          ----> cors
          ----> body-parser
          ----> express
          ----> sqlite
          ----> sqlite3
          ----> bcryt
          ----> jsonwebtoken
          
----> #assignmentDatabase(assignment.db) is created

----> in assignmentDatabase two table are present with the help of sqlite3
          ----> users
          ----> todo

----> in user table the following column represents
          ----> id
          ----> username
          ----> password

          ---> below contains the sqlite3 of users

          CREATE TABLE "todo" ("id"	INTEGER NOT NULL,"user_id"	INTEGER,
	        "todo"	varchar(255),"description"	TEXT,"status"	varchar(255),
	        "priority"	varchar(255),PRIMARY KEY("id" AUTOINCREMENT),
	        FOREIGN KEY("user_id") REFERENCES "users");
         
----> in todo table the following column represents 
          ----> id
          ----> user_id
          ----> todo
          ----> description
          ----> priority
          ----> status

          ---> below contains sqlite3 of todo

          CREATE TABLE "users" ("id"	INTEGER NOT NULL,"username"	varchar(255),
	        "password"	varchar(255),PRIMARY KEY("id" AUTOINCREMENT));
          
----> middileware is used in to access the user's resources

----> authentication and autherization is used with the help of following libraries 
          in order to access the token or get the token
	  ----> jsonwebtoken --> sign --> verify 
	  
          ----> bcrypt --> hash -->compare

----> deployed backend API is 
### https://backendtodoblog2-4.onrender.com

----> the above API is implemented in
### https://main--nucleartodo.netlify.app

----> CRUD operations are used which are mention below:-
        
### POST http://localhost:4000/register

--> the above POST method is used to register the new user details if the user is already register then it response's user already exit's

### POST http://localhost:4000/login

--> the above POST method is used to login the user credentials which is stored in the database 

### POST http://localhost:4000/todos

--> the above POST method is used to add new TODO details to the database

### GET http://localhost:4000/todos/?priority=''&search=''

--> the above GET method is used to get the tododata of the user and also queried with #priority and #search

### PUT http://localhost:4000/todos/:id

--> the above PUT method is used to UPDATE the todoData of the user

### PUT http://localhost:4000/status/:id

--> the above PUT method is used to update the status of the tododata

### DELETE http://localhost:4000/todos/:id

--> the above DELETE method is used to DELETE the tododata of the corresponding id

                 **** in order to understand more and clear check out the index.js which i commented for each functions and Api *****


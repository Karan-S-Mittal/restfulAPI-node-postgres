# RESTful API - Node - PostgreSQL

This application is REST API performing CRUD operations using postgreSQL Database.<br>The application integrates nodejs and postgresql.

# Installation

```Powershell
node index.js
```
You should have nodejs and postgreSQL installed to run this application.

Execute these commands one by one to in <strong>psql shell</strong>.

1. Make a new User named <b>me</b>. givig him permission to create database.
    ```SQL
    CREATE ROLE me WITH LOGIN PASSWORD 'password';
    ALTER ROLE me CREATEDB;
    ```
2. Login with the user <b>me</b> by restarting the shell/session.

3. Create a new Database named API while logged in as user <b>me</b>.
    ```SQL
    CREATE DATABASE api;
    ```

4. Use that database.
    ```
    \c api
    ```

5. Create a new Table
    ```SQL
    CREATE TABLE users (
    ID SERIAL PRIMARY KEY,
    name VARCHAR(30),
    email VARCHAR(30)
    )
    ```

6. Add some random values (optional)
    ```
    INSERT INTO users (name, email)
    VALUES ('Karan', 'karan@example.com'), ('Shyam', 'shyam@example.com'), ('Ali', 'Ali@example.com');
    ```
> pro tip: if you found errors in the code above, check your commas. postgreSQL takes `'` and not `"`.


# Author
Karan Mittal

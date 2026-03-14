# Application Analysis

The lab provides a vulnerable web application which interacts with a backend SQL database.

The application constructs SQL queries using user input without proper sanitization.

Example query used by the application:

SELECT uid, name, profileID, salary, passportNr, email, nickName, password
FROM usertable
WHERE profileID=10 AND password='ce5ca67...'

Because the user input is directly inserted into the query, it becomes vulnerable to SQL Injection.

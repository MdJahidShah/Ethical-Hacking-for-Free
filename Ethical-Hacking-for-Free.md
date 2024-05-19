<h1>Ethical Hacking for Free</h1>
<p align="center">
  <img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg"> <img src="https://img.shields.io/github/stars/payloadbox/sql-injection-payload-list?style=social"> <img src="https://img.shields.io/github/forks/payloadbox/sql-injection-payload-list?style=social"> <img src="https://img.shields.io/github/repo-size/payloadbox/sql-injection-payload-list"> <img src="https://img.shields.io/github/license/payloadbox/sql-injection-payload-list"> <img src="https://img.shields.io/github/issues/detail/author/payloadbox/command-injection-payload-list/1">
</p>

### Basic SQL Injection Theory
<p>
SQL injection is a type of security vulnerability that occurs when an attacker can manipulate an SQL query by injecting malicious input into a query. This can allow the attacker to view, modify, or delete data in a database, bypass authentication mechanisms, and in some cases, execute administrative operations on the database server.

** Here’s a basic overview of SQL injection theory:**

#### 1. Understanding SQL Injection
SQL injection exploits vulnerabilities in web applications that take user input and include it directly in SQL queries without proper validation or sanitization. This happens when input fields, such as login forms, search bars, or URL parameters, are used to construct SQL queries dynamically.

#### 2. Types of SQL Injection
* Classic SQL Injection: The attacker inputs malicious SQL code into a user input field to manipulate the query.
* Blind SQL Injection: This occurs when the application does not return error messages or query results to the attacker. Instead, the attacker infers information based on the application’s behavior.
* * Boolean-based Blind SQL Injection: Uses true/false conditions to determine if the payload executed successfully.
* * Time-based Blind SQL Injection: Relies on database delays to infer query results.
*  Error-based SQL Injection: Leverages detailed error messages from the database server to gather information about the database structure.
*  Union-based SQL Injection: Uses the UNION SQL operator to combine results from multiple SELECT statements into a single result set.
#### 3. Basic SQL Injection Example
Consider a simple login form where the user inputs a username and password. The backend might construct an SQL query like this:

```
SELECT * FROM users WHERE username = 'user' AND password = 'pass';
```
If the application does not properly sanitize inputs, an attacker can input the following:

<b>Username: admin'--</br>
Password: anything</b>
The resulting query would be:

```
SELECT * FROM users WHERE username = 'admin'--' AND password = 'anything';
```

The -- marks the start of a comment in SQL, so the rest of the query is ignored. This effectively becomes:

```
SELECT * FROM users WHERE username = 'admin';
```
If the username 'admin' exists, the attacker gains access without needing a valid password.

#### 4. Consequences of SQL Injection
* **Unauthorized Data Access:** Attackers can retrieve sensitive data.
* **Data Manipulation:** Attackers can modify or delete data.
* **Privilege Escalation:** Attackers can gain administrative privileges.
* **Denial of Service:** Attackers can disrupt database services.
* **Data Integrity and Confidentiality Breach:** Compromised data can lead to loss of trust and legal consequences.
#### 5. Prevention Techniques
* **Input Validation and Sanitization:** Ensure that user inputs are validated and sanitized. Use allowlists and disallowlists to filter out dangerous characters.
* **Parameterized Queries (Prepared Statements):** Use placeholders in SQL queries instead of concatenating user inputs directly.
* **Stored Procedures:** Encapsulate SQL queries within stored procedures to reduce the risk of injection.
* **Least Privilege Principle:** Restrict database user permissions to only what is necessary for the application.
* **Web Application Firewalls (WAF):** Use WAFs to detect and block SQL injection attempts.
* **Regular Security Testing:** Perform regular security audits, code reviews, and vulnerability assessments.
#### 6. Example of Parameterized Query
**Using parameterized queries in languages like PHP with PDO:**

```
$stmt = $pdo->prepare('SELECT * FROM users WHERE username = :username AND password = :password');

$stmt->execute(['username' => $username, 'password' => $password]);
```

This approach ensures that user inputs are treated as data, not executable code, mitigating the risk of SQL injection.

By understanding and implementing these principles, developers can significantly reduce the risk of SQL injection in their applications.</p>

#### Generic SQL Injection Payloads

```
1" OR "1" = "1
1' OR '1' = '1
' OR 'x'='x
' AND id IS NULL; --

'''''''''''''UNION SELECT '2

```

#### Generic Error Based Payloads

```
 Cooming Soon...
```

#### Generic Time Based SQL Injection Payloads

```
Cooming Soon...

```
### Resources

* [Basic SQL Injection Google Dork List](https://github.com/MdJahidShah/SQL-Injection-Google-Dork-List/blob/main/Basic-SQL-Injection-Google-Dork-List.html)

#### SQL Injection Vulnerability Scanner Tool's :

* [SQLMap](https://github.com/sqlmapproject/sqlmap) – Automatic SQL Injection And Database Takeover Tool

* [jSQL Injection](https://github.com/ron190/jsql-injection) – Java Tool For Automatic SQL Database Injection

* [BBQSQL](https://github.com/Neohapsis/bbqsql) – A Blind SQL-Injection Exploitation Tool

* [NoSQLMap](https://github.com/codingo/NoSQLMap) – Automated NoSQL Database Pwnage

* [Whitewidow](https://www.kitploit.com/2017/05/whitewidow-sql-vulnerability-scanner.html) – SQL Vulnerability Scanner

* [DSSS](https://github.com/stamparm/DSSS) – Damn Small SQLi Scanner

* [explo](https://github.com/dtag-dev-sec/explo) – Human And Machine Readable Web Vulnerability Testing Format

* [Blind-Sql-Bitshifting](https://github.com/awnumar/blind-sql-bitshifting) – Blind SQL-Injection via Bitshifting

* [Leviathan](https://github.com/leviathan-framework/leviathan) – Wide Range Mass Audit Toolkit

* [Blisqy](https://github.com/JohnTroony/Blisqy) – Exploit Time-based blind-SQL-injection in HTTP-Headers (MySQL/MariaDB)
    <h2>Contact Us</h2>
    <ul>
        <li><a href="https://www.linkedin.com/in/md-jahid-shah-js/" target="_blank">Linkedin</a></li>
    </ul>
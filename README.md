# The project’s primary goals consist of:
A robust and effective web based online banking system.

Extending functionality without compromising the security.

Personal banking services that gives you complete control over all your banking demands online.

Simple and easy user interface to work with.

# Online Banking features:
Registration for online banking by Admin.

Adding Beneficiary account by customer.

Transferring amount to the beneficiary added by customer.

Staff must approve for beneficiary activation before it can be used for transferring funds.

Customer gets to know his last login date and time each time he logs in.

Customer can check last 10 transactions made with their account.

Customer can check their account statement within a date range.

Customer can request for ATM and Cheque Book.

Staff will approve requests for ATM card and cheque book.

Admin can add/edit/delete customer as well as staff.

All three of them(customer, staff & admin) can change their password.

Staff and Admin Login pages are hidden from customer for security purpose.

Security:
Each and every input is passed through mysql_real_escape_string() to remove special characters from the string so that user can’t submit arbitrary input. It protects from attacks like Sql Injection and Cross Site Scripting(XSS).

Passwords are encrypted with SHA- 1 hashing algorithm and then stored in database.

Passwords are stored as encrypted hashes with an additional random salt for added security.


Database:
The database contains customer, staff & admin tables.

Each customer has its own virtual passbook linked with its account number.

Staff, customer and, admin have their details and password in their respective tables with all the details.

A separate table for beneficiary is included in the database.

A table for cheque book and ATM requests is included.

This project is divided into three hierarchical parts:

The index page for the customer login.

A hidden staff login page.

A hidden admin login page.

Usage:
1.Install XAMPP or something similar.

2.Copy all the files to c:/xampp/htdocs/banking/

3.Create a db named as 'bnak_db' and import the bank_db.sql from phpMyAdmin.

4.change the password in _inc/dbconn.php file accordingly.

5.visit localhost/banking (customer index page)

6.visit localhost/banking/adminlogin.php (admin login)

7.visit the localhost/banking/staff_login.php (staff login)

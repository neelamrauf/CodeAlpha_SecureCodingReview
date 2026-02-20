Secure Coding Review
Objective
To perform a manual code review of a Python script to identify security vulnerabilities and provide remediation steps.

Vulnerability Identified: SQL Injection
In the vulnerable_code.py file, the get_user function uses direct string formatting to build a database query. This allows an attacker to manipulate the query and gain unauthorized access to data.

Remediation (The Fix)
The code should be updated to use Parameterized Queries. This ensures that user input is treated as data only, not as executable code.

Secured Code Snippet:
Python
# Secured Version
def get_user_secure(username):
    query = "SELECT * FROM users WHERE username = ?"
    cursor.execute(query, (username,))
Conclusion
Documenting these findings helps in building resilient systems and ensures safer code deployment.

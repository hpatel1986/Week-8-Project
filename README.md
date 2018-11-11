# Week 8 Project: Pentesting Live Targets
Time spent: **4** hours spent in total

### Objective: The goal is to identify which two vulnerabilities the blue target has, which two vulnerabilities the green target has, and which two vulnerabilities the red target has.

The possible exploits are:

[x] Username Enumeration
[x] Insecure Direct Object Reference (IDOR)
[x] SQL Injection (SQLi)
[] Cross-Site Scripting (XSS)
[x] Cross-Site Request Forgery (CSRF)
[x] Session Hijacking/Fixation


## Green
### Vulnerability #1: User Enumeration ###

<img src='https://i.imgur.com/opBVKdl.gif' title='User Enumeration' width='' alt='User Enumeration' />

When I used a non-existing user, the site gave me a unsuccessful login. But when you use an existing user with a random password the error message gets displayed in bold.


## Red
### Vulnerability #1: Insecure Direct Object Reference ###

<img src='https://i.imgur.com/5lUMpUB.gif' title='Insecure Direct Object Reference' width='' alt='Insecure Direct Object Reference' />

Just modified the salesperson URL with "?id=", with this you can access records 10 and 11.

### Vulnerability #2: Cross-Site Request Forgery ###

<img src='https://i.imgur.com/9nqgTSE.gif' title='Insecure Direct Object Reference' width='' alt='Insecure Direct Object Reference' />
The site accepts a post request from a different source that has a hidden form in it, and makes alterations to the user database.


## Blue
### Vulnerability #1: SQL injection ###

<img src='https://i.imgur.com/BNC5f6O.gif' title='SQL Injection' width='' alt='SQL Injection' />

In the URL, you insert "?id=XX" and change the color in the URL to red or green. Inserting blue results in page error, resulting from the query being not able to connect to the DB.

### Vulnerability #2: Session Hijacking/Fixation ###

<img src='https://i.imgur.com/W6XzJ2s.gif' title='Session Hijacking' width='' alt='Session Hijacking' />

Used the target's session, you can change the session ID to get the same login creds.



# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: * SQL Injection (SQLi) - When logged in, on the staff menu, appending the blind injection ' OR SLEEP(5)=0--' on the end of the url showing a specific salesperson, causes the server to wait.
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/sqli.gif)

Vulnerability #2: * Session Hijacking/Fixation
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/hijack.gif)




## Green

Vulnerability #1: * Username Enumeration - Upon valid username submition, the error message displayed is bold, however, an invalid username submition is not bold.  The developer used span class failed instead of failure.
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/username_enumeration.gif)

Vulnerability #2: * Cross-Site Scripting (XSS) - Contect form. <script>alert('Mallory found the XSS!');</script>  When logged in and visiting the feedback page, the alert pops.
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/xss.gif)

## Red

Vulnerability #1: * Insecure Direct Object Reference (IDOR) - On the salesperson.php page, the system will return employees in the DB who are no longer or not yet sales person.  Blue/green redirect to the sales person page if no territories are assigned to a salesperson.
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/idor.gif)

Vulnerability #2: * Cross-Site Request Forgery (CSRF) - By creating a custom HTML page with a hidden form, and submitting it to the feedback page.
![Lab 1 gif](https://github.com/justinw238/codepath_8_jlw15/blob/master/csrf.gif)


## Notes

Describe any challenges encountered while doing the work

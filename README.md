# Reviewing SQL Logs


<h2>Description</h2>
In this project, our team was tasked with finding information on daily issues. We explore how to find login attempts and later look at employees to resolve any further issues. Through this project, I show my fluency with SQL and relational databases.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Bash</b>
- <b>SQL</b>

<h2>Environments Used </h2>

- <b>Linux</b> 

<h2>Walk-through:</h2>

<p align="left">
Retrieve after hours failed login attempts: <br/>
<img src="https://i.imgur.com/Jk4XhDs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
To retrieve the after-hour failed attempts, we must check the log_in_attempt file. The file contains all log-ins, and to get the information we want, we must provide the time that is considered after hours, in this case, after 6 PM or 18:00. Then make sure the success is FALSE, which shows the attempt was unsuccessful. 
<br />
<br />

Retrieve login attempts on specific dates:<br />
<img src="https://i.imgur.com/IBXH2mY.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
We found a breach on May 9th, 2022.  We know breaches are usually not isolated in one day, so we are also looking at the previous day. We filter based on the login_date column and add both days using the OR key. There are 75 records to view the above screenshot is a small portion.
<br />
<br />

Retrieve login attempts outside of Mexico:<br />
<img src="https://i.imgur.com/nVv7Ew1.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
We now know that logins were not originating in Mexico, so we must filter the country out. To do that, we use the NOT key and the LIKE key. The not key was used to exclude nonrelevant information. The LIKE key was used with ‘MEX%’ to capture all variations of Mex, MEX., Mexico, etc.
<br />
<br />

Retrieve employees in Marketing:<br />
<img src="https://i.imgur.com/iQsD8et.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
We are looking for Marketing employees in the east wing. To do this, we must search in the employee table, so we change the FROM to employees.  Then we must add the filters we know must be in Marketing, so we find all Marketing people based on the department column. Then, we must find all people on the east wing using LIKE as there are variations. The following instructions give the screenshot above. 
<br />
<br />

Retrieve employees in Finance or Sales:<br />
<img src="https://i.imgur.com/9eIZ5f2.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
We are tasked with updating all Sales and FInance devices. To do this, we must find all employees and then filter on those two departments. We can achieve this by using the OR key and typing in both departments, then running the query. There are 71 records the screenshot above is not all-inclusive.
<br />
<br />

Retrieve all employees not in IT:<br />
<img src="https://i.imgur.com/q9sv6at.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/><br />
The team was tasked with acquiring all people not in IT as they had repaired their own equipment. To find all the employees, we must search the employee table and use the NOT key. Instead of WHERE we USE WHERE NOT, then type in the department. There are 161 records listed in the full table the above screenshot is incomplete.
<br />
<br />


Summary:  <br/>
SQL is very useful when trying to combat security risks. Thus, being familiar with it is a key quality to have.  Through this project, we have explored many ways to use keys to find specific information, which is vital for forensic reports. Many other uses for SQL would benefit your company and its security.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

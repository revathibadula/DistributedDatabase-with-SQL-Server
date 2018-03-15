Use a Linked Server Without a Database Reference
Linked servers are configured to enable the Database Engine to execute a Transact-SQL statement that includes tables in another instance of SQL Server, or another database product such as Oracle. Many types OLE DB data sources can be configured as linked servers, including Microsoft Access and Excel.
Steps to follow:	
•	Create a dummy table-valued function (TVF) that defines the result set from the query that uses a linked server; e.g. create the TVF, but do not return any rows
•	ALTER the TVF in the post-deployment script; put in the select statement that references the linked server
•	Create a new view to select from the TVF

 We have queried stored procedures  in linked server:
i.	Create stored procedures:
(a)	Without parameters
(b)	With parameters
ii.	Alter stored procedures
iii.	Add a database reference to your project which requires that you create a DACPAC file. : A DACPAC file (also known as a Data-tier application) is defined as "a logical database management entity that defines all of the SQL Server objects - like tables, views, and instance objects, including logins – associated with a user’s database. A DAC is a self-contained unit of SQL Server database deployment that enables data-tier developers and database administrators to package SQL Server objects into a portable artifact called a DAC package, also known as a DACPAC".

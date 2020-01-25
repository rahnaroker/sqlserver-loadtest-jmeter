# sqlserver-loadtest-jmeter
upwork very first task

1. Download JMeter
https://jmeter.apache.org/download_jmeter.cgi

2. Download JDBC MS SQL Driver
https://docs.microsoft.com/ru-ru/sql/connect/jdbc/download-microsoft-jdbc-driver-for-sql-server?view=sql-server-ver15

3. Run JMeter 

4. Open Test.jmx

5. Check path to JDBC MS SQL Driver in 'Test Plan' root tree element
Default: C:\temp\proj\libs\mssql-jdbc-7.4.1.jre8.jar

6. Update connection to your SQL Database in JDBC Connection Configuration tree element

7. Update variables in 'User Defined Variables' tree element:
TOTAL_AMOUNT_OF_ROWS - number of rows to fullfill database before test
TOTAL_AMOUNT_OF_INSERTED_ROWS - number of rows to insert in test
TOTAL_AMOUNT_OF_UPDATED_ROWS - number of rows to update in test

8. Run Test to fullfill database via 'Thread Group - Initial' tree element

9. Comment 'Thread Group - Initial'

10. Uncomment 'Thread Group - INSERT', 'Thread Group - UPDATE', 'Thread Group - DELETE'

11. Run Test load database by inserting, updating and deleting rows
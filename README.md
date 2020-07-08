# Oracle-1Z0-931   <p>       </p>  <img src="images/logo2.JPG" alt="logo2.JPG" style="zoom:20%;" />

## Comprehensive cheat sheet to pass Oracle 1Z0-1085 Exam

------

Data Pump:
----------
- Can exclude migration of objects like indexes and materialized views that are not needed by Autonomous Database.
- Faster to migrate database than using RMAN


Data Sync:
----------
- Data Sync can load a combination of data source, such as .csv, .xlsx and Oracle relational files.
- Data Sync can connect to any jdbc compatible source like MongoDB, Redshift and Sybase.
- Perform incremental data loads or rolling deletes.
- Perform insert-only or append strategies.
- Transform your data.
- Schedule data loads.


Golden Gate:
-------------
- You can configure the Autonomous Database instance as a target database for Oracle GoldenGate On Premises.
- You can’t set up Oracle Autonomous Database Cloud database as a source database for Oracle GoldenGate On Premises.
- Only the migration to ADB is possible from an on-premise installation of Golden Gate.


SQL Developer:
---------------
- SQL Developer can be used to export/move/import of a databases to ADB in 1 set of wizard steps.
- SQL Developer can import .csv files into ADB which are located on the system where SQL Developer is running.
- SQL Developer can import files (.dmp and .csv for example) into ADB which are located on Amazon S3 Object storage.


DBMS_CLOUD.COPY_DATA
---------------------
- If your source files reside in Oracle Cloud Infrastructure Object Storage Classic, the username is your Oracle Cloud Infrastructure Classic user name and the password is your Oracle Cloud Infrastructure Classic password
- If your source files reside in Amazon S3 or you are calling an AWS API, the username is your AWS access key ID and the password is your AWS secret access key
- If your source files reside in Azure Blob Storage or you are calling an Azure API, the username is your Azure storage account name and the password is an Azure storage account access key.
- A valid credential must be created prior to running the DBMS_CLOUD.COPY_DATA procedure.


The Wallet file include:
------------------------
- tnsnames.ora
- sqlnet.ora
- cwallet.sso
- keystore.jks
- odbc.properties
- README

Two Security Feature Enabled by default:
----------------------------------------
- SQL Net Encryption
- Transparent Data Encryption

Two methods of migration from on-premise:
-----------------------------------------
- Data Pump
- Golden Gate

Three methods of Loading data to ADB:
-------------------------------------
- Data Pump
- Golden Gate
- SQL*Loader

When Autonomous Database is stopped:
------------------------------------
- Tools are no longer able to connect to a stopped instance.
- CPU billing is halted based on full cycle of usage.
- In-flight transactions and queries are stopped.


Two system Privileges to create analytic views:
-----------------------------------------------
- CREATE ATTRIBUTE DIMENTION
- CREATE ANALYTIC VIEW

Validate Analytic View:
-----------------------
- VALIDATE_ANALYTIC_VIEW
- VALIDATE_HIERARCHY


Three data dictionary views contain information about analytic view objects
-----------------------------------------------------------------------------
- ALL_ANALYTIC_VIEW_DIM_CLASS
- ALL_ANALYTIC_VIEW_LVLGRPS
- ALL_ANALYTIC_VIEW_KEYS

Two options to restore:
------------------------
- Specify the point in time (timestamp) to restore
- Select the backup from which restore needs to be done.

Two tasks can be executed from the service console:
----------------------------------------------------
- Autonomous Databases monitoring for usage and query performance.
- Wizard to download connection wallet for connection from desktop tools.


Two methods can you use to define Machine Learning Users
--------------------------------------------------------
- SQL/Developer
- Oracle Cloud Infrastructure Console

Two methods can you use to create users and grant roles in ADB
---------------------------------------------------------------
- SQL/DeveloperSQLPlus

- SQLPlus


DBMS_CLOUD:
--------------
- **DELETE_FILE Procedure:**
  This procedure removes the specified file from the specified directory on Autonomous Data Warehouse.
- **CREATE_CREDENTIAL Procedure:**
  This procedure stores Cloud Object Storage credentials in the Autonomous Data Warehouse database. Use stored credentials for data loading or for querying external data residing in the Cloud.
- **PUT_OBJECT Procedure:**
  This procedure copies a file from Autonomous Data Warehouse to the Cloud Object Storage. The maximum file size allowed in this procedure is 5 gigabytes (GB).
- **VALIDATE_EXTERNAL_TABLE Procedure:**
  This procedure validates the source files for an external table, generates log information, and stores the rows that do not match the format options specified for the external table in a badfile table on Autonomous Data Warehouse.
- **CREATE_EXTERNAL_TABLE Procedure:**
  This procedure creates an external table on files in the Cloud. This allows you to run queries on external data from Autonomous Data Warehouse.


ANALYTIC VIEW:
---------------
- **CREATE ANALYTIC VIEW:**
  Create an analytic view in the grantee's schema.
- **CREATE ANY ANALYTIC VIEW:**
  Create analytic views in any schema except SYS.
- **CREATE ATTRIBUTE DIMENSION:**
  Create an attribute dimension in the grantee's schema.
- **CREATE ANY ATTRIBUTE DIMENSION:**
  Create attribute dimensions in any schema except SYS.
- **CREATE HIERARCHY:**
  Create a hierarchy in the grantee's schema.
- **CREATE ANY HIERARCHY:**
  Create hierarchies in any schema except SYS.
- **ALTER ANY ANALYTIC VIEW:**
  Rename analytic views in any schema except SYS.
- **ALTER ANY ATTRIBUTE DIMENSION:**
  Rename attribute dimensions in any schema except SYS.
- **ALTER ANY HIERARCHY:**
  Rename hierarchies in any schema except SYS.
- **DROP ANY ANALYTIC VIEW:**
  Drop analytic views in any schema except SYS.
- **DROP ANY ATTRIBUTE DIMENSION:**
  Drop attribute dimensions in any schema except SYS.
- **DROP ANY HIERARCHY:**
  Drop hierarchies in any schema except SYS.
- **SELECT ANY TABLE:**
  Query or view any analytic view or hierarchy in any schema

Miscellaneous:
---------------

- When scaling OCPUs Active Transactions continue running unaffected.
- Ignores hints in SQL Statements by default **-->** ADW
- Security features that are available in Oracle Autonomous Database **-->** Data Redaction & TDE
- REST verb is used to create an Autonomous Database service using REST APIs **-->** A "POST" REST call
- predefined user is created when an Autonomous Database (ADB) instance is created **-->** ADMIN
- predefined role in ADB **-->** DWROLE
- features is NOT part of the Autonomous Database **-->** Java in Database
- NOT automatically performed **-->** Mask Sensitive Data
- Modify default 8 days retention period for performance data in DBMS_WORKLOAD_REPOSITORY **-->** MODIFY_SNAPSHOT_SETTINGS
- Provision resource without logging in **-->** CLI + REST API call
- Set HTTP Proxy in JDBC **-->** tnsnames.ora
- Add user's public ssh key in console **-->** Identity --> Select User --> Add Public Key
- Oracle allow you to scale compute and storage independently.
- Connect Oracle Analytics Cloud to the Autonomous Data Warehouse, you need to upload **-->** CWALLET.SSO
- NOT required to connect to Autonomous Database from SQL developer **-->** Database Name
- Default Port Number to connect ADB **-->** 1522
- OCPU and Storage can scale independently.
- operating system can Data Visualization Desktop be run on **-->** Windows + MAC
- Import tables into the Oracle Analytics Cloud (OAC) **-->** Create a Data Set
- JDBC Thin client versions earlier than 18.1 do not support connections through HTTP proxy
  subset of services offered via OCI-CLI **-->** Create, Get, List, Stop, Restore.
- Default retention period for both Automatic and Manual Autonomous Database Backups **-->** 60 days
- Low provides highest concurrency, lowest resources, and DoP =1
- The Way SQL Developer help you test your data loading scenario **-->** In the Column Definition Phase, the system cross-references with the file-contents and shows the conflicts with the definition.

------

**1Z0-1085:**
https://www.udemy.com/course/1z0-1085-20-oraclecloudinfrastructurefoundationsassociate

**1Z0-1067:**
https://www.udemy.com/course/oracle-cloud-infrastructure-cloud-operations-associate/

**1Z0-1072:**
https://www.udemy.com/course/1z0-1072-oracle-cloud-infra-architect-associate/

**1Z0-1084:**
https://www.udemy.com/course/oracle-cloud-infra-developer-2020-associate-practice-test/

**1Z0-931:**
https://www.udemy.com/course/oracle-autonomous-database-cloud-specialist-1z0-931-practice-test/

**1Z0-997:**
https://www.udemy.com/course/1z0-997-oracle-cloud-infrastructure-architect-professional-k



**Note:** For Active Coupon please contact us through below mail id 

------

**Contact Us:**

[digitechcloud20@gmail.com]()



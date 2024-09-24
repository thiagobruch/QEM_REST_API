Please find below the instructions to use Postman with QEM APIs:

1 - Download and install Postman from:
https://www.getpostman.com/

2 - Once the app is installed and running, go to File and click on Import:
 
Import both files attached to the email.

3 – On the Top Right of the screen, click on the drop down next to “No Environment” and select QEM
4 – Click on the eye symbol   and under QEM click on Edit

5 – Edit all the variables as the instructions below (the names are case sensitive)

session_id: you do not have to edit this one, it will generate an ID once you execute the QEM Login
aem_server: your QEM Server (IP address or DNS Name)
replicate_server: The name of your Replicate Server configured in QEM
endpoint_source: A Source Endpoint that is already configure in the Replicate Server mentioned above
endpoint_target: A Target Endpoint that is already configure in the Replicate Server mentioned above
task_name: A task name that is already configured in your Replicate Server
schema_name: In order to reload a table, use a schema name that is part of the task above
table_name: In order to reload a table, use a table name that is part of the task and schema above

8 – Click on Save and close the next window

9 – Go to File, Settings and under General, turn off “SSL Certificate Verification” and close the window.

10 – Go to Collections, click on the QEM Login. Under Authorization, select Basic Auth and type the username and password as the example below:
bruch-qem\administrator (where bruch-qem is the server name and administrator is the username)

11 – Click on Save and Send.
You should have a response similar to the example below:

Content-Length →0
Content-Type →text/html
Date →Thu, 06 Apr 2022 19:34:55 GMT
EnterpriseManager.APISessionID →yUgwAp80FFtdq2R5E_YxQg
Server →Microsoft-HTTPAPI/2.0

12 – The QEM Login, has to be executed every time the Postman program is opened.
This will get the ID for that session and store for 5 minutes.

All the other commands can be execute and the result can be found under “body”.
To run each command click on the command under Collections and click on Send.

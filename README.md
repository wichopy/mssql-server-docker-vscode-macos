# Microsoft SQL Server + Docker + VS Code + MacOS

This repo is a reference for connecting to and developing with MS SQL Server in a MacOS / VS Code / Docker environment.

## Run Image

From the Microsoft docs:
https://docs.microsoft.com/en-ca/sql/linux/quickstart-install-connect-docker?view=sql-server-linux-2017

`docker run -e ACCEPT_EULA=Y -e SA_PASSWORD=[YOUR_STRONG_PASSWORD] -e MSSQL_PID=Express -p 1433:1433 --name [YOUR_CONTAINER_NAME] microsoft/mssql-server-linux`

## Connect to database using docker + bash:

`docker exec -it [YOUR_CONTAINER_NAME] bash`

`/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P '[YOUR_STRONG_PASSWORD]'`

## VS Code mssql extension:
From the Microsoft docs:
https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-develop-use-vscode?view=sql-server-linux-2017

Create a new profile cmd + shift + P > MS SQL: Connect
Follow prompts for database configurations

Open script file and hit cmd + shift + E to execute a query.

Have the option to right click on results and save queries as json

## Sample Scripts

This repo contains some very basic scripts to create a data base, create a table, insert into a table, and select from a table.

Try executing scripts from the docker bash and within VS Code using the mssql extension.

Important: Each script needs to start with a USE [TABLE_NAME] for the script to execute.

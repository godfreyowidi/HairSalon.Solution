## _Eau Claire's Saloon_

## _Description_

This web application offers the user an opportunity to interact with Eau Claire's Salon services. It also provides Eau Claire's Salon manager an opportunity to assign her clients to a specific stylist depending on their order. The manager can also see a list of all clients with their respective assigned stylist according to their area of speciality.

## _Technologies Used_

* C#
* ASP.NET Core MVC
* Entity Framework
* MySql Workbench
* HTTP RESTful Routing
* Git/GitHub

## _Setup Requirements_

* Browser
* Code Editor (preferrably vsCode)
* ASP.NET Core installed
* Terminal

## _Installation_

_Use the browser to navigate to GitHub page respository Click the Green Code button on the right and select Download Zip._

_Alternatively clone from Github via the terminal using ```git clone``` command In your terminal, navigate to the directory where you would like to clone the project to._

_Clone this repo to your chosen directory using this link "https://github.com/godfreyowidi/HairSalon.Solution" in terminal_

* **Setting Up the Database**

```Using Workbench```

_Launch MySql Workbench 8.0CE and click on create a new schema to add a new database_

_Create new table(s) each representing the project class_

_Right click on each of the table(s) to choose alter table and add properties while assigning each of them values according to its nature_

_Click apply and finish when done to set up the database_

```Using terminal```

_First, log in to the MySql server using a user account that has the ```CREATE DATABASE``` privilege by entering the command ```mysql -u root -p```._

_Authenticate by entering the password for the ```root``` user and then proceed by pressing ```Enter```._

_Next, show the databases available on the server using the ```SHOW DATABASES```_

```
+--------------------+
| Database           |
+--------------------+
| example_datab      |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.00 sec)
```
_Then, issue the ```CREATE DATABASE``` command with a database name i.e ```CREATE DATABASE hair_salon;``` and press ```Enter```_

_It will return the following ```Query OK, 1 row affected (0.02 sec)```_

_After that, use the ```SHOW CREATE DATABASE hair_salon``` to review the created database_

_You will receive the database name plus the character set and collation of the database_
```
+----------+----------------------------------------------------------------------------------------------------------------------------------+
| Database | Create Database                                                                                                                  |
+----------+----------------------------------------------------------------------------------------------------------------------------------+
| testdb  | CREATE DATABASE `hair_salondb` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */ |
+----------+----------------------------------------------------------------------------------------------------------------------------------+
1 row in set (0.01 sec)
```
_Finally, select the database by ```USE hair_salon``` and it will return ```Database changed```_

_Quit mysql by running ``exit``_

* **.NET Environment Setup**

_After opening the project and before setting up the dependencies and tools for the project, add the file appsettings.json to the project root directory by running the command ```touch appsettings.json```. Click on the file and add the following:_
```
{
    "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=[YOUR-USERNAME-HERE];uid=root;pwd=[YOUR-PASSWORD-HERE];"
    }
}
```
_This is a connection string and database will change based on which one we are connecting to. Replace [YOUR-USERNAME-HERE] and [YOUR-PASSWORD-HERE] with the name of your database schema and database login password_

_Because this file will contain sensitive information, it is imperative to add it to ```.gitignore`` file before making any commits_

* **If you chose to download via zip:**

_Unzip the downloaded repository into your working directory_

_Open the working directory into your code editor using the command ```code .```_

_Once you have the program open in your code editor, run ```dotnet restore``` inside the production directory to set up the dependencies and tools for the project._

_After the project is sucessfully set up, navigate to the directory in the terminal. Then execute the command ```dotnet run``` or ```dotnet watch run``` to start server_

* **If you cloned via Git:**

_Using the terminal, navigate to the directory the project is located using ```cd HairSalon.Solution```_

_Open the working directory in your code editor using the ```code .``` command._

_From the terminal, ```run dotnet restore``` in the terminal to set up the dependencies and tools for the project._

_After the dependencies and tools for the project are sucessfully set up, navigate to the HairSalon directory in the terminal._

_Execute the commmand ```dotnet run``` or ```dotnet watch run``` to start the server._

* **Using the application:**

_Server is started on either :-_

_http://localhost:5000_

_http://localhost:5001_

_Copy and paste either of the above in the browser to experience the splash page_

_You can follow along and create a stylist and then assign a client them._

_You can also search for specific stylist and client using the unique ID and it will be displayed in the browser_

_The application is also able to update and edit stylists and clients details as well as clear list of stylists and clients and also delete/destroy stylists and clients entries_

_Overally the application uses CRUD functionality as way to Create, Read, Update and Delete/Destroy information into persisent storage_


## _Known Bugs_
no known bugs

## _License_
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## _Contact_
[Email Contact](godfreyowiidi@gmail.com)
# Contract-Management-API-.NET-
A **Contract Management System** built using **ASP.NET MVC / Web API** with a **3-tier N-Tier architecture** (Presentation Layer, Business Logic Layer, Data Access Layer). The system provides APIs for managing users, contacts, and authentication with features like CSV import/export, birthday reminders, and duplicate contact deletion.

---

## Features

### Authentication
- User login and logout.
- Token-based authentication.
- Secured APIs using custom `[Logged]` attribute.

### Contact Management
- CRUD operations: Create, Read, Update, Delete contacts.
- Search contacts by name and email.
- Group contacts by category.
- Export contacts to CSV.
- Upload contacts from CSV.
- Birthday reminders via email.
- Delete duplicate contacts.

### User Management
- CRUD operations for users.
- Integrated with authentication service.

---

## Technology Stack

- **Backend**: ASP.NET Web API, C#  
- **Architecture**: N-Tier (Presentation, BLL, DAL)  
- **Database**: SQL Server / Entity Framework  
- **Other Technologies**: AutoMapper, JWT, CSV handling, Email Notifications  

---

## Project Structure
Contract_Management_System/
- Contract_Management_System.sln
- packages.config
- Contract_Management_System/          (Presentation Layer - API)
    - Controllers/
- Business_Logic_Layer/                (BLL)
    - DTOs/
    - Services/
- Data_Access_Layer/                    (DAL)
    - Repos/

---

## Installation

1. Clone the repository:
```bash
git clone https://github.com/rubayitalam/Contract-Management-System.git
Open solution in Visual Studio 2019/2022.

Restore NuGet packages:

dotnet restore


Build the solution:

dotnet build


Update the Web.config connection string to your database.

Run the application.Contacts
#######API ######## API ####### 
Authentication
Method	Endpoint	Description
POST	/api/login	Login user
POST	/api/logout	Logout user
Method	Endpoint	Description
GET	/api/contact/getall	Get all contacts
GET	/api/contact/get?id={id}	Get contact by ID
POST	/api/contact/create	Create new contact
POST	/api/contact/update	Update existing contact
GET	/api/contact/delete?id={id}	Delete contact by ID
GET	/api/contact/searchbyname?name={name}	Search by name
GET	/api/contact/searchbyemail?email={email}	Search by email
GET	/api/contact/groupbycategory	Group contacts by category
GET	/api/contact/exporttocsv	Export all contacts to CSV
POST	/api/contact/uploadcsv	Upload contacts from CSV
GET	/api/contact/birthdayreminder	Send birthday reminders
GET	/api/contact/deleteduplicate	Delete duplicate contacts
Users
Method	Endpoint	Description
GET	/api/User/getall	Get all users
GET	/api/User/get?id={id}	Get user by ID
POST	/api/User/create	Create new user
POST	/api/User/update	Update user
GET	/api/User/delete?id={id}	Delete user by ID

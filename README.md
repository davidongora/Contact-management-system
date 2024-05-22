# Contacts Management System

This is a Contacts Management System built with Laravel. The application allows users to perform CRUD operations on contacts and group them into categories like "Family" and "Friends".

## Features

- Add, edit, and delete contacts.
- Group contacts into categories.
- View a list of all contacts and groups.

## Prerequisites

- PHP (>= 8.1)
- Composer
- MySQL
- Node.js & npm
- Git

## Setup Instructions

Follow these steps to set up and run the project on your local machine.

### Step 1: Clone the Repository

```sh
git clone https://github.com/your-username/contacts-management-system.git
cd contacts-management-system

composer install
npm install
Step 3: Environment Configuration
Copy the example .env file to create your own configuration file.


cp .env.example .env
Update the .env file with your database credentials and other necessary settings:

env code
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_username
DB_PASSWORD=your_database_password


Step 4: Generate Application Key

php artisan key:generate
Step 5: Run Migrations and Seeders
Ensure your database is running, then execute the following commands to set up the database schema and seed initial data:


php artisan migrate --force
php artisan db:seed --class=GroupSeeder --force
Step 6: Run the Application
Start the Laravel development server:


php artisan serve
Run the Vite development server:


npm run dev
Step 7: Access the Application
Open your browser and navigate to:



http://127.0.0.1:8000

Project Structure

Controllers: Handles the business logic of the application.
ContactController.php
GroupController.php
Models: Represents the data structure.
Contact.php
Group.php
Views: Blade templates for the frontend.
resources/views/contacts
resources/views/groups
Migrations: Database schema.
database/migrations/xxxx_xx_xx_create_contacts_table.php
database/migrations/xxxx_xx_xx_create_groups_table.php
Seeders: Initial data seeding.
database/seeders/GroupSeeder.php
Routes: Web routes for the application.
routes/web.php


Usage
Contacts:
Create a new contact: Navigate to /contacts/create and fill in the details.
Edit a contact: Click the "Edit" button next to a contact on the contacts list page.
Delete a contact: Click the "Delete" button next to a contact on the contacts list page.

Groups:
Groups are automatically seeded with "Family" and "Friends".
Contacts can be assigned to these groups when created or edited.


Approach
Laravel Blade Templates: Used for the frontend to maintain simplicity and quick development.
Eloquent ORM: Utilized for database operations.
Validation and Error Handling: Implemented to ensure data integrity and provide user feedback.

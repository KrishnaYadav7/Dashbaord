This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
video:

https://github.com/user-attachments/assets/c5cec54e-b4dd-4a53-bfea-bb2bfc8d26ad



You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

Dashboard Application
This repository contains a dashboard application built using Next.js. The application includes various layouts such as "Dashboard", "Analytics", "Users", "Settings", "Help" (with subcategories "Message" and "Trash"), and "Project". The backend is powered by MySQL using Laragon. The application supports CRUD operations for users, visualization with pie charts, and notifications using Toastify. The frontend uses MUI (Material-UI) for components and icons.

Table of Contents
Features
Tech Stack
Installation
Database Setup
Running the Application
Project Structure
Layouts and Pages
CRUD Operations
Charts and Analytics
Notifications
Contributing
License
Features
Multiple layouts: Dashboard, Analytics, Users, Settings, Help (Message, Trash), and Project.
CRUD operations: Add, edit, update, and delete users.
Data visualization: Pie charts for user analytics.
User statistics: Active users, new users, total users, and returning users.
Notifications: Toastify integration for notifications.
Tech Stack
Frontend:
Next.js
MUI (Material-UI)
Toastify
Backend:
MySQL (using Laragon)
Next API Routes
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/your-repo-name.git
Navigate to the project directory:
bash
Copy code
cd your-repo-name
Install the dependencies:
bash
Copy code
npm install
Database Setup
Install Laragon and start it.
Create a new MySQL database:
sql
Copy code
CREATE DATABASE dashboard_db;
Import the provided SQL schema (located in the database folder):
bash
Copy code
mysql -u root -p dashboard_db < database/schema.sql
Configure the database connection in your environment variables. Create a .env.local file in the root directory and add:
env
Copy code
DATABASE_HOST=localhost
DATABASE_USER=root
DATABASE_PASSWORD=yourpassword
DATABASE_NAME=dashboard_db
Running the Application
Start the development server:
bash
Copy code
npm run dev
Open your browser and navigate to http://localhost:3000.
Project Structure
plaintext
Copy code
├── components
│   ├── Layouts
│   ├── Charts
│   ├── Users
│   └── Notifications
├── pages
│   ├── api
│   │   └── users
│   ├── dashboard
│   ├── analytics
│   ├── users
│   ├── settings
│   ├── help
│   │   ├── message
│   │   └── trash
│   └── project
├── public
├── styles
├── utils
│   └── db.js
└── .env.local
Layouts and Pages
Dashboard: Overview of key metrics and notifications.
Analytics: Pie charts and user statistics.
Users: List, add, edit, and delete users.
Settings: Application settings.
Help:
Message: User messages.
Trash: Deleted items.
Project: Project-related information and management.
CRUD Operations
CRUD operations are implemented for user management. The API endpoints are located in the pages/api/users directory.

Add User
Endpoint: POST /api/users
Request Body:
json
Copy code
{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "status": "active"
}
Edit User
Endpoint: PUT /api/users/[id]
Request Body:
json
Copy code
{
  "name": "Jane Doe",
  "email": "jane.doe@example.com",
  "status": "inactive"
}
Delete User
Endpoint: DELETE /api/users/[id]
Get Users
Endpoint: GET /api/users
Charts and Analytics
Pie charts are used to visualize user data. The charts are located in the components/Charts directory and use data fetched from the backend.

Notifications
Toast notifications are implemented using Toastify. Notifications are triggered for actions like adding, editing, and deleting users.

Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Feel free to customize this README as per your specific project requirements.

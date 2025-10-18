# 📬 Reachinbox Web Application

## 🚀 Overview
The **Reachinbox Web Application** is a powerful email management platform built with a user-friendly interface. It enables users to efficiently manage their emails, view detailed threads, compose replies, and toggle between light and dark themes.  
The app seamlessly integrates with **Reachinbox APIs** to fetch and manage real-time email data.

---

## ✨ Features

- **📂 Sidebar Navigation** – Quick access to various app sections.  
- **🧭 TopBar** – Displays current workspace and includes a theme toggle.  
- **📧 Main Page** – Lists email threads and shows detailed views of selected emails.  
- **🧑‍💼 Right Section** – Displays lead details and activity history.  
- **🪄 SubView** – Placeholder screen when there are no emails.  
- **✉️ Custom Mail** – Allows composing and sending replies.  
- **🗑️ Delete PopUp** – Confirmation before deleting an email.  
- **🌗 Theme Toggle** – Switch between Dark and Light mode.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/saqlainkaleem/reachinbox.git


# Navigate to the Project Directory

cd reachinbox

## Install Dependencies

npm install

## Start the Development Server

npm run dev


The application will be available at http://localhost:5173

## 🔗 API Endpoints
# List Email Threads

- **Endpoint: GET /api/v1/onebox/list
- **Description: Retrieves a list of email threads.
- *Headers:

- **Authorization: Bearer <token>

# Reply to an Email Thread

- **Endpoint: POST /api/v1/onebox/reply/{threadId}
- **Description: Sends a reply to the specified email thread.
- *Headers:

- **Authorization: Bearer <token>


- **Request Body:

{
  "to": "recipient@example.com",
  "from": "sender@example.com",
  "subject": "Subject of the email",
  "body": "Body of the email"
}

## Reset Email Data

- **Endpoint: GET /api/v1/onebox/reset
- **Description: Resets the email data (useful for testing).
- *Headers:

- **Authorization: Bearer <token>

## 🧩 Components
# SideBar

- ** Description: Fixed sidebar for navigation with section icons (Home, Mail, Search).

- *Props:

- **onMenuItemClick(Function) – Handles menu item click events.

- *State:

- **selectedItem – Tracks currently selected menu item.

# TopBar

- **Description: Displays app title and workspace name, includes a theme toggle.

- *Features:

- **Dark/Light mode toggle.

# MainPage

- **Description: Core area with email threads, selected thread details, and extra info.

- *State:

- **datas – List of fetched email threads.

- **loading – Loading status indicator.

- **selectedThread – Currently viewed email thread.

# RightSection

- **Description: Displays lead details and activities related to the selected email.

- *Features:

- **Lead info (name, email, LinkedIn).

- **Recent email activity timeline.

# SubView

- **Description: Placeholder shown when no emails are available.

- *Features:

- **Displays an image and “No Emails” text.

# CustomMail

- **Description: Compose and send replies to existing email threads.

- *State:

- **replyData – Contains to, from, subject, body fields.

# DeletePopUp

- **Description: Popup for confirming email deletion.

- *Props:

- **onCancel(Function) – Cancel action handler.

- **onDelete(Function) – Confirm deletion handler.

# ThemeToggle

- **Description: Toggles between dark and light themes.

- *State:

- **darkMode (Boolean) – Current theme mode.

## 🛠️ Tech Stack

- **Frontend: React + Vite

- **Language: TypeScript

- **Styling: Tailwind CSS

- **API Integration: Reachinbox REST APIs

- **State Management: React Hooks / Context API
# SQL Queries API Lab

**Author:** *Tomas Enrico NIsay*  

---

## 📖 Overview
This project demonstrates how SQL queries can be integrated into a Node.js/Express API.  
It explores different database operations such as joins, unions, cross joins, and full outer join emulation.  
Endpoints are tested with **Postman** against a **MySQL** database.  

---

## 🛠️ Tech Stack
- **MySQL** – Relational database  
- **SQL** – Query language  
- **Node.js / Express** – Backend framework  
- **Postman** – API testing tool  

---

## 🚀 Features
- Retrieve the latest login per user  
- Show referral relationships between users  
- Generate all possible user-role pairings  
- Emulate a full outer join with UNION  
- Display roles with or without assigned users  
- Fetch users together with their profile information  
- List users with their corresponding roles  

---

## ⚙️ Installation
1. Install and configure a MySQL database (local or cloud).  
2. Import the provided SQL scripts into your database.  
3. Install Node.js dependencies:  
   ```bash
   npm install

---

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|------------|
| `/api/reports/users-with-roles` | GET | List all users with their assigned roles (INNER JOIN). |
| `/api/reports/users-with-profiles` | GET | List all users with profiles, including users without profiles (LEFT JOIN). |
| `/api/reports/roles-right-join` | GET | List roles with assigned users, including roles with no users (RIGHT JOIN). |
| `/api/reports/profiles-full-outer` | GET | Emulate full outer join for users and profiles (LEFT + RIGHT JOIN with UNION). |
| `/api/reports/user-role-combos` | GET | Generate all possible user-role combinations (CROSS JOIN). |
| `/api/reports/referrals` | GET | Show referral relationships (SELF JOIN / INNER JOIN). |
| `/api/reports/latest-login` | GET | Retrieve each user’s most recent login IP and timestamp (LEFT JOIN + subquery). |

## Query Types Overview

- **INNER JOIN:** Users with roles  
- **LEFT JOIN:** Users with profile info  
- **RIGHT JOIN:** Roles with users (including empty roles)  
- **LEFT + RIGHT JOIN UNION:** Full outer join emulation  
- **CROSS JOIN:** All user-role combinations  
- **SELF JOIN (INNER JOIN):** Referral relationships  
- **LEFT JOIN + Subquery:** Latest login per user  

## Usage

- Run API endpoints to explore query results.  
- Test outputs in Postman.  
- Learn SQL joins, unions, and backend data workflows.

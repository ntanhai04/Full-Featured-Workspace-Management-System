# 🚀 Full-Featured Workspace Management System (v5.0)

A full-featured workspace management platform built with PHP and MySQL.  
The system uses a two-role model: **Guardian** (workspace owner) and **Individual** (workspace member).  
Version **5.0** includes advanced features such as notifications, tags, file attachments, rewards, approval workflow, and progress reporting.

---

## 👥 Roles

### 🛡 Guardian
Workspace owner, manages members, rewards, approvals.

### 👤 Individual
Creates goals and tasks, uploads work, submits tasks for approval, earns points.

---

## 🗂 Workspace & Members
- Workspace creation and ownership  
- Member management  
- Role-based permissions  

---

## 🎯 Goals & Tasks
- Long-term goals  
- Short-term tasks with:
  - 📝 Title, description
  - 📅 Due date (DATETIME)
  - ⚡ Priority (Low / Medium / High)
  - 🔁 Recurrence rules
  - 🏷 Multiple tags
- Status workflow:  
  **⭕ To Do → 🕒 Pending Approval → ✅ Approved / ❌ Request Changes**

---

## 💬 Comments & 📎 Attachments
- 💭 Comment system for each task  
- 📤 Upload files (images, documents)  
- 📁 File metadata stored in `task_attachments`  

---

## 🔔 Notification System
Notifications are triggered for:
- 💭 New comments  
- 📤 Task submitted for approval  
- ✅ Task approved  
- ❌ Task rejected  
- ⏰ Deadline reminders (cron job)  
- 🎁 Reward redemption requests  

---

## 🏷 Tags System
- Guardian creates tags (🖍 name + 🎨 color)  
- Tasks can have multiple tags  
- 🔍 Filter tasks by tag or priority  

---

## 🎁 Reward System
- Guardian creates rewards  
- Individuals earn ⭐ points when tasks are approved  
- Individuals can redeem rewards  
- Guardian approves redemption requests  

Tables include:  
- `rewards`  
- `user_points`  
- `redeemed_rewards`  

---

## ✔️ Approval Workflow
- Individual submits task ➜ Guardian gets a notification  
- Guardian reviews:
  - ✅ **Approve** → Points awarded  
  - ❌ **Request Changes** → Task returned with required comment  

---

## 📊 Progress Reports
Includes:
- 📈 Task completion rate  
- ⏳ Overdue tasks  
- ⭐ Points earned  
- 🏷 Tag distribution  

---

## 🗄 Database Structure
Includes tables for:
- 👥 Users  
- 🗂 Workspaces & Members  
- 🎯 Goals  
- 📝 Tasks  
- 💬 Comments  
- 📎 Attachments  
- 🏷 Tags  
- 🔔 Notifications  
- 🎁 Rewards & Points  

---

## 🛠 Technology
- **PHP** (Backend)  
- **MySQL** (Database)  
- Designed to be simple, modular, and extendable  


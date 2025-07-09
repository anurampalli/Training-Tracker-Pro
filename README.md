# 📘 Training Tracker Pro

**Training Tracker Pro** is a scoped application built on the ServiceNow platform to help organizations manage and monitor employee training activities efficiently. This academic project showcases key platform features such as custom tables, references to existing tables, email notifications, reports, and dashboards.

---

## 📌 Project Highlights

- 🎯 Track training sessions and employee participation
- 📧 Automated email notifications to employees and trainers
- 📊 Generate reports on attendance and training completion
- 📋 Visual dashboard for quick insights
- 🔁 Built entirely in ServiceNow Studio and committed to GitHub

---

## 📁 Application Scope

- **Application Name:** Training Tracker Pro
- **Scope Identifier:** `x_ttpro`
- **Platform:** ServiceNow (Scoped Application)
- **Type:** Academic / Demonstration Project

---

## 📊 Data Model

### 🟢 `Training Session [x_1778869_ttp_training_session]`
Custom table to define training sessions.

| Field | Type | Description |
|-------|------|-------------|
| Session ID | Auto Number | Unique identifier |
| Session Name | String | Title of the session |
| Trainer | Reference (`sys_user`) | Trainer assigned |
| Department | Reference (`cmn_department`) | Relevant department |
| Scheduled Date | Date/Time | When the session will occur |
| Description | HTML | Details about the session |
| Status | Choice | Scheduled / Completed / Cancelled |

---

### 🟢 `Training Record [x_1778869_ttp_training_record]`
Tracks participation of employees in sessions.

| Field | Type | Description |
|-------|------|-------------|
| Employee | Reference (`sys_user`) | Participant |
| Training Session | Reference (`x_ttpro_training_session`) | Linked session |
| Attendance Status | Choice | Attended / Absent / Excused |
| Completion Date | Date | When training was completed |
| Score | Integer | Optional evaluation score |
| Feedback | String | Optional remarks |

---

## ✉️ Email Notifications

### 1. Session Scheduled Notification
- **Trigger:** New session created
- **Recipients:** All employees in the session's department
- **Content:** Session details (name, date, trainer)

### 2. Attendance Confirmation
- **Trigger:** Training Record updated to "Attended"
- **Recipient:** Employee
- **Content:** Thank you message + feedback form link

---

## 📈 Reports

1. **Training Completion Rate by Department**
   - Bar chart showing % of employees with completed trainings per department

2. **Training Session Attendance Breakdown**
   - Pie chart showing Attended / Absent / Excused distribution for each session

---

## 📊 Dashboard

A dashboard titled **"Training Tracker Dashboard"** includes:
- The two reports mentioned above
- Filter controls for department and session date range

---

## 🔧 Technical Components

| Component | Included |
|----------|-----------|
| Custom Tables | ✅ |
| Reference Fields | ✅ (`sys_user`, `cmn_department`) |
| Email Notifications | ✅ |
| Business Rules / Flows | ✅ |
| Reports | ✅ |
| Dashboard | ✅ |
| Update Set Export | ✅ |
| GitHub Integration | ✅ |

---

## 🧠 Learning Outcomes

- Creating a scoped application in ServiceNow
- Defining and referencing custom tables
- Creating email layout and template
- Creating email notification
- Enabling email sending in ServiceNow
- Configuring Flow Designer for emails
- Designing reports and dashboards
- Using GitHub with ServiceNow Studio

---

## 🌐 How to Use

1. Clone or fork this repo
2. Import the update set into your ServiceNow instance
3. Navigate to Studio to view and customize
4. Test email triggers and validate reports
5. Share your dashboard with stakeholders!

---

## 🤝 Credits

Developed by **Anasuya Rampalli**  
Academic/Portfolio Project – ServiceNow Platform

---

## 🔗 LinkedIn 

www.linkedin.com/in/anurampallichitta



---


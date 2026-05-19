# 🏫 ISMS - Integrated School Management System

## Software Requirements Analysis & Business Documentation

[![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)](https://github.com/)
[![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)](https://github.com/)
[![Documentation](https://img.shields.io/badge/Documentation-Full-orange?style=for-the-badge)](https://github.com/)
[![Business Analysis](https://img.shields.io/badge/Business-Analysis-purple?style=for-the-badge)](https://github.com/)

---

## 📖 How to View This Project

### Option 1: Download the PDF (Save to your computer)

[![Download PDF](https://img.shields.io/badge/⬇️-DOWNLOAD_PDF-red?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://github.com/habiba-ahmed9/ISMS-Project-Software-Requirements-Analysis/raw/main/ISMS%20Software%20Requirements%20Analysis.pdf)

Click the button above to **download** the PDF file directly to your computer.

---

### Option 2: View Online (Open in browser)

[![View PDF](https://img.shields.io/badge/👁️-VIEW_ONLINE-blue?style=for-the-badge&logo=github&logoColor=white)](https://github.com/habiba-ahmed9/ISMS-Project-Software-Requirements-Analysis/blob/main/ISMS%20Software%20Requirements%20Analysis.pdf)

Click the button above to **view** the PDF directly in your browser.



## 📌 Project Overview

**Future Vision International School (FVIS)** is a private K-12 institution experiencing rapid growth in student enrollment, staff recruitment, and academic program expansion. However, the school continues to operate through **manual paperwork, disconnected Excel spreadsheets, and isolated software tools** that do not communicate with one another.

This **Integrated School Management System (ISMS)** project provides a complete business analysis and system design to transform FVIS operations into a **centralized, digital, and automated environment**.

---

## 📊 The 8 Business Problems Solved

| # | Problem | Impact |
|---|---------|--------|
| 1 | No centralized student data repository | Data duplication, retrieval delays |
| 2 | Manual attendance recording | No real-time visibility, delayed notifications |
| 3 | Error-prone grade management | Inaccurate grades, delayed report cards |
| 4 | Inefficient manual fee collection | Reconciliation errors, fraud risk |
| 5 | Poor parent communication | Delayed critical notifications |
| 6 | No strategic reporting | Reports take days to compile |
| 7 | Manual scheduling conflicts | Timetable conflicts, resource waste |
| 8 | No digital document storage | Data loss risk, slow retrieval |

---

## 🎯 Business Objectives & Success Criteria

| ID | Objective | Target | Timeline |
|----|-----------|--------|----------|
| OBJ-01 | Eliminate paper-based student records | 100% digital | Go-Live |
| OBJ-02 | Reduce attendance recording errors | ≥99% accuracy | 3 months |
| OBJ-03 | Automate fee processing | ≥60% reduction | 6 months |
| OBJ-04 | Accelerate grade reporting | ≤48 hours | Term 1 |
| OBJ-05 | Increase parent engagement | ≥80% active users | 6 months |
| OBJ-06 | Enable real-time decision-making | Weekly usage | Go-Live |
| OBJ-07 | Achieve high system availability | ≥99.5% uptime | Ongoing |
| OBJ-08 | Ensure scheduling efficiency | 0 conflicts | Term 1 |

---


---

## 🏗️ System Modules (12 Core Modules)

| # | Module | Description |
|---|--------|-------------|
| 1 | Student Registration & Information Management | Centralized student profiles, document upload, unique ID |
| 2 | Teacher & Staff Management | Staff profiles, class/subject assignments, directory |
| 3 | Class Enrollment & Academic Structure | Academic years, semesters, class sections, scheduling |
| 4 | Attendance Recording | Digital attendance with real-time parent notifications |
| 5 | Exam & Grade Management | Grade entry, automatic GPA, report cards, exam scheduling |
| 6 | Fee Payment Processing | Online payments, invoices, receipts, overdue reminders |
| 7 | Parent & Student Portals | Dashboards for grades, attendance, fees, communication |
| 8 | Reporting & Dashboards | Real-time KPIs for principal and board |
| 9 | Role-Based Access Control | Permissions per user role (Admin, Teacher, Student, Parent) |
| 10 | Notifications & Alerts System | Multi-channel alerts (SMS, email, in-app) |
| 11 | Audit & Activity Tracking | Immutable logs of all system actions |
| 12 | System Interface & Language Support | Arabic (RTL) and English (LTR) support |

---

## 📐 System Diagrams

### 1. Class Diagram (Page 26)

![Class Diagram](class-diagram.jpeg)

*UML Class Diagram showing all entities in the Integrated School Management System*

**Entities (Classes) in the diagram:**

| Class | Key Attributes |
|-------|----------------|
| **Student** | studentID, fullName, dateOfBirth, gender, address, email, phone, enrollmentDate, academicHistory |
| **Teacher** | teacherID, name, specialization, email, phone |
| **Parent** | parentID, fullName, relation, phone, email, address |
| **Grade** | gradeID, score, GPA |
| **Attendance** | attendanceID, date, status |
| **Exam** | examID, title, type, date, deadline |
| **Payment** | paymentID, amount, paymentMethod, paymentDate |
| **Invoice** | invoiceID, amount, dueDate, paymentStatus |
| **ClassSection** | classID, className, capacity |
| **Subject** | subjectID, subjectName, credits |
| **Enrollment** | enrollmentID, enrollmentDate, status |
| **UserAccount** | username, password, role, isLoggedIn |
| **Role** | roleID, roleName, permissions |
| **Notification** | notificationID, type, message, sentDate |
| **Message** | messageID, sender, content, timestamp |
| **ReportCard** | reportID, resultDate, remarks |

**Relationships shown:**
- Student ↔ Enrollment ↔ ClassSection ↔ Subject ↔ Teacher
- Student ↔ Grade ↔ Exam
- Student ↔ Attendance
- Student ↔ Parent
- Student ↔ Invoice ↔ Payment
- UserAccount ↔ Role (RBAC)

---

### 2. Behavioral Diagram (Page 27)

![Behavioral Diagram](behavioral-diagram.png)

*Sequence/Activity Diagram illustrating interaction flow between actors and system components*

**Actors & Components in the flow:**

| Actor/Component | Role |
|-----------------|------|
| **Student** | Initiates actions (login, view details, get confirmation) |
| **Teacher** | Manages grades, submits reports, updates information |
| **Admin** | Configures settings, manages system |
| **Application Server** | Processes requests, handles business logic |
| **Database (DB)** | Stores and retrieves data |
| **Document Storage** | Stores files and documents |
| **Parent Notification System** | Sends alerts to parents |
| **Scheduling Engine** | Manages timetable and appointments |

**Key Flows:**

1. **Student Flow:** Login → Enter personal details → Verification → Data input → Configuration → Confirmation → Feedback

2. **Teacher Flow:** Status check → Record details → Verification → Submit to report center → Update information → Delete notifications

3. **Parent Notification Flow:** Application Server → Database → Parent Notification System → Notification alerts to parents

4. **Scheduling Flow:** Scheduling Engine → Schedule appointments → Conflict detection → Finalize timetable

**Alternative Flows:**
- Error handling for failed connections
- Verification failures with retry options
- Notification delivery status tracking

---

## ✅ In-Scope Features (Version 1.0)

| ID | Feature | Linked Objective |
|----|---------|------------------|
| S-01 | Student Information Management | OBJ-01 |
| S-02 | Teacher & Staff Management | OBJ-02 |
| S-03 | Academic Year & Class Configuration | OBJ-04 |
| S-04 | Attendance Recording & Notifications | OBJ-02 |
| S-05 | Grade & Exam Management | OBJ-04 |
| S-06 | Fee Structure & Invoice Management | OBJ-03 |
| S-07 | Online Fee Payment | OBJ-03 |
| S-08 | Parent Portal | OBJ-05 |
| S-09 | Student Portal | OBJ-05 |
| S-10 | Executive Dashboard & Reporting | OBJ-06 |
| S-11 | Role-Based Access Control (RBAC) | OBJ-07 |
| S-12 | Audit Logs & Automated Backups | OBJ-07 |
| S-13 | Bilingual Interface (Arabic/English) | OBJ-05 |

---

## ❌ Out-of-Scope (Deferred to Future Releases)

| ID | Excluded Feature | Reason |
|----|------------------|--------|
| X-01 | Native Mobile Apps (iOS/Android) | Web responsive sufficient for v1.0 |
| X-02 | Learning Management System (LMS) | Beyond administrative scope |
| X-03 | Ministry of Education Integration | Requires external approval |
| X-04 | AI-Powered Predictive Analytics | Insufficient historical data |
| X-05 | Library Management Module | Separate operational domain |

---

## 👥 Stakeholder Analysis

### Power vs. Interest Matrix

| Category | Stakeholders | Engagement Strategy |
|----------|--------------|---------------------|
| **High Power / High Interest** | School Board, Principal, Head of Finance, IT Manager | Manage Closely - Regular meetings, approvals |
| **High Power / Low Interest** | Ministry of Education, Payment Gateway Provider | Keep Satisfied - Monitor, ensure compliance |
| **Low Power / High Interest** | Teachers, Parents, Students, Administrative Staff | Keep Informed - Training, feedback sessions |

---

## 📊 14 Use Cases Included in PDF

| # | Use Case | Primary Actor |
|---|----------|---------------|
| 1 | Record and Edit Attendance | Teacher |
| 2 | Create Exams, Quizzes, Assignments | Teacher |
| 3 | Record and Update Student Grades | Teacher |
| 4 | View Personal Grades | Student |
| 5 | View Attendance Record | Student |
| 6 | View Child's Grades | Parent |
| 7 | Communicate with Teachers | Parent |
| 8 | Create and Manage Student Profiles | Administrator |
| 9 | Generate and Manage Timetables | Administrator |
| 10 | Generate Invoices | Administrator |
| 11 | Track Fee Payments | Administrator |
| 12 | Send Overdue Payment Reminders | System (Automated) |
| 13 | Perform Database Backups | System (Automated) |
| 14 | Switch Interface Language | All Users |

---

## 🛠️ Non-Functional Requirements

| Category | Requirement | Target |
|----------|-------------|--------|
| **Performance** | Student record retrieval | ≤2 seconds |
| **Performance** | Report card generation | ≤5 seconds per student |
| **Performance** | Dashboard loading | ≤3 seconds |
| **Reliability** | Attendance accuracy | ≥99% |
| **Availability** | System uptime | ≥99.5% |
| **Security** | Data encryption | SSL/TLS |
| **Scalability** | Maximum students | 5,000+ |
| **Backup** | Recovery time | ≤1 hour |

---




## 📄 License

This project is for educational purposes as part of a Business Analysis / Software Requirements course.

---

## ⭐ Show Your Support

If you found this project helpful or interesting, please **star** ⭐ this repository!

---

> 📌 *"Transforming manual school operations into an integrated digital ecosystem."*

---

### 🔗 Connect With Us

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/habiba-ahmed-5043a6374)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:h.ahmed3885@gmail.com)

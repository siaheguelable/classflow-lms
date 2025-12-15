# Mini-Toddle (IB-Style Learning Management System)

## 📘 Project Overview

Mini-Toddle is a **Toddle-inspired Learning Management System (LMS)** designed to model how IB schools manage classes, teachers, and students. The system follows **strict role-based access control**, where **only the Super Admin** can create classes, assign teachers, and enroll students.

This project is built for **learning, portfolio, and academic purposes**. It is **not a clone** of Toddle, but a simplified system inspired by its workflows.

---

## 🎯 Project Goals

* Practice **full-stack development**
* Implement **role-based access control (RBAC)**
* Build a **real-world education platform**
* Demonstrate understanding of **IB school workflows**
* Produce a **portfolio-ready project**

---

## 👥 User Roles & Permissions

### 🛡️ Super Admin

The Super Admin has full control over the system.

* Create classes
* Assign teachers to classes
* Enroll students into classes
* View all classes and users

### 👨‍🏫 Teacher

Teachers can only manage academic content.

* View assigned classes
* Create assignments
* View student submissions

❌ Cannot create classes
❌ Cannot enroll students

### 👩‍🎓 Student

Students can only access their learning materials.

* View enrolled classes
* View assignments
* Submit assignments

❌ No class or user management

---

## 🔐 Access Control Rules (RBAC)

| Action            | Super Admin | Teacher | Student |
| ----------------- | ----------- | ------- | ------- |
| Create class      | ✅           | ❌       | ❌       |
| Assign teacher    | ✅           | ❌       | ❌       |
| Enroll student    | ✅           | ❌       | ❌       |
| Create assignment | ❌           | ✅       | ❌       |
| Submit assignment | ❌           | ❌       | ✅       |

---

## 🛠️ Tech Stack

### Frontend

* React
* Tailwind CSS
* React Router (protected routes)

### Backend

* Node.js
* Express.js

### Database

* MongoDB
* Mongoose

### Authentication

* JWT (JSON Web Tokens)
* Password hashing

---

## 🗂️ Project Structure

```
mini-toddle/
│
├── client/                # React frontend
│   ├── pages/
│   │   ├── admin/
│   │   ├── teacher/
│   │   └── student/
│   ├── components/
│   └── services/
│
├── server/                # Backend
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── middleware/
│   └── config/
│
└── README.md
```

---

## 🗃️ Database Models (Initial)

### User

* name
* email
* password
* role (super_admin | teacher | student)

### Class

* name
* teacherIds[]
* studentIds[]

### Assignment

* title
* description
* dueDate
* classId

### Submission

* assignmentId
* studentId
* content
* submittedAt

---

## 🌐 API Endpoints (Planned)

### Super Admin

* POST /classes
* PUT /classes/:id/assign-teacher
* PUT /classes/:id/enroll-student

### Teacher

* GET /classes/my-classes
* POST /assignments

### Student

* GET /classes/my-classes
* POST /submissions

---

## 🚀 Development Phases

### Phase 1: Authentication & Roles

* User registration (admin creates users)
* Login system
* Role-based route protection

### Phase 2: Class Management (Admin)

* Create classes
* Assign teachers
* Enroll students

### Phase 3: Assignments (Teacher)

* Create assignments
* View submissions

### Phase 4: Student Interaction

* View assignments
* Submit work

### Phase 5: UI & Polish

* Improve dashboard UI
* Error handling
* Basic validation

---

## ⚠️ Disclaimer

This project is **for educational and portfolio use only**.

* No Toddle branding is used
* No proprietary features are copied
* All design and code are original

---

## 📌 Author

**Curtis**
Software Development Student | Educator | IB Certified

---

## ✅ Status

🚧 Project initialized – README created

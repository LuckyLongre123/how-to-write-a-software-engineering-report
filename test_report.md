# 📋 Software Engineering Problem Statement & System Analysis Report

## Student Result Management System
### B.Voc Software Development Programme — University Academic Division

---

[![Document Type](https://img.shields.io/badge/Document-Problem%20Statement%20%26%20System%20Analysis-blue)](.)
[![Status](https://img.shields.io/badge/Status-Draft%20v1.0-orange)](.)
[![Prepared For](https://img.shields.io/badge/Prepared%20For-Software%20Development%20Company-purple)](.)
[![Academic Year](https://img.shields.io/badge/Academic%20Year-2025--26-green)](.)

---

> **Document Classification:** Internal — Academic Project Proposal  
> **Prepared By:** University Academic Systems Committee  
> **Prepared For:** Contracted Software Development Company  
> **Date:** April 2026  
> **Version:** 1.0  
> **Programme Scope:** B.Voc Software Development (All Semesters)

---

## 📑 Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Problem Statement & Process Model](#2-problem-statement--process-model)
   - 2.1 [Current System Overview](#21-current-system-overview)
   - 2.2 [Problem Statement](#22-problem-statement)
   - 2.3 [Proposed Solution Overview](#23-proposed-solution-overview)
   - 2.4 [Process Model Selection](#24-process-model-selection)
3. [Stakeholder Analysis](#3-stakeholder-analysis)
4. [Scope of the Project](#4-scope-of-the-project)
5. [System Objectives](#5-system-objectives)
6. [Requirement Analysis](#6-requirement-analysis)
   - 6.1 [Functional Requirements](#61-functional-requirements)
   - 6.2 [Non-Functional Requirements](#62-non-functional-requirements)
   - 6.3 [Data Flow Diagram (DFD)](#63-data-flow-diagram-dfd)
   - 6.4 [Data Dictionary](#64-data-dictionary)
   - 6.5 [Use Case Diagram & Descriptions](#65-use-case-diagram--descriptions)
7. [Project Management](#7-project-management)
   - 7.1 [Function Point Analysis](#71-function-point-analysis)
   - 7.2 [Effort Estimation](#72-effort-estimation)
   - 7.3 [Project Schedule & Gantt Overview](#73-project-schedule--gantt-overview)
   - 7.4 [Risk Table](#74-risk-table)
8. [Design Engineering](#8-design-engineering)
   - 8.1 [Architectural Design](#81-architectural-design)
   - 8.2 [Data Design (Database Schema)](#82-data-design-database-schema)
   - 8.3 [Component-Level Design (Pseudocode)](#83-component-level-design-pseudocode)
9. [Benefits of the Proposed System](#9-benefits-of-the-proposed-system)
10. [Constraints and Assumptions](#10-constraints-and-assumptions)
11. [Possible Risks](#11-possible-risks)
12. [Conclusion and Recommendations](#12-conclusion-and-recommendations)

---

## 1. Executive Summary

The university currently manages student academic results for the **B.Voc Software Development Programme** through a combination of paper-based registers, Microsoft Excel spreadsheets, and informal email communications. This fragmented and manual approach leads to chronic deficiencies: delayed result publication, frequent data-entry errors, difficulty in generating consolidated transcripts, and an absence of real-time performance visibility for students, faculty, and administration.

This document constitutes the formal **Problem Statement and System Analysis Report**, prepared to commission a professional software development company to design, develop, test, and deploy a purpose-built **Student Result Management System (SRMS)**. The proposed system will digitise and automate the complete results lifecycle — from the entry of marks by faculty, through multi-level administrative approval, to the secure publication of results accessible to students via a web portal and mobile interface.

The SRMS will serve all stakeholders of the B.Voc Software Development programme across all six semesters, handling course-wise internal assessment marks, end-semester examination marks, attendance integration, grade calculation, backlog tracking, and the generation of official mark sheets and transcripts.

This report covers the full software engineering analysis including:
- Detailed problem identification
- Functional and non-functional requirements
- Stakeholder mapping
- Data Flow Diagrams (DFD)
- Data Dictionary
- Use Case Descriptions
- Function Point Analysis and Effort Estimation
- Risk Assessment
- Architectural and Database Design blueprints
- Pseudocode for key system components

---

## 2. Problem Statement & Process Model

### 2.1 Current System Overview

The B.Voc Software Development programme spans **three academic years** divided into **six semesters**, with each semester containing multiple theory and practical courses. Each course is evaluated through:

- **Internal Assessment (IA):** Three internal tests per semester (best two considered), practical records, assignments, and attendance-based marks.
- **End-Semester Examination (ESE):** A central university-level written and/or practical examination.
- **Final Grade:** Computed as a weighted combination of IA (40%) and ESE (60%) scores.

Under the **existing manual system**, the process operates broadly as follows:

| Phase | Current Manual Process |
|---|---|
| **Mark Entry** | Faculty records internal marks on paper mark-lists and submits to the department office. |
| **Compilation** | Administrative staff manually transcribes marks into department-maintained Excel sheets. |
| **Verification** | HOD manually cross-checks individual sheets. No automated validation. |
| **ESE Marks** | University examination cell sends ESE scores via emailed Excel files. Staff manually merges these with IA data. |
| **Grade Calculation** | Staff manually applies grading formulae. Errors are frequent and go undetected. |
| **Result Publication** | Printed result lists are posted on a physical notice board. Students must visit in person. |
| **Transcripts & Mark Sheets** | Manually typed and printed; no automated generation. Subject to delays of weeks. |
| **Backlog Management** | Tracked in separate registers; easy to misplace or overlook. |
| **Data Archiving** | Old semester data stored in physical files; prone to loss and damage. |

This procedure is deeply inefficient, error-prone, and unsuitable for a technology-oriented programme like B.Voc Software Development, where students expect and deserve a seamless digital academic experience.

---

### 2.2 Problem Statement

> *"The current manual result management system for the **B.Voc Software Development Programme** suffers from **chronic data-entry errors, weeks-long delays in result publication, lack of real-time access, inability to audit grade changes, disorganised backlog management, and zero integration between internal assessment and end-semester examination data**. As a result, **students** face anxiety and uncertainty awaiting results published on notice boards, **faculty** spend disproportionate time on administrative tasks rather than teaching, and **administrative staff** bear an unsustainable clerical burden with no data validation safety net. Therefore, we propose the development of a **Student Result Management System (SRMS)** — a centralised, secure, web-based application that will **automate mark entry, enforce validation rules, calculate grades in real time, publish results instantly online, generate official mark sheets and transcripts on demand, and provide comprehensive analytics dashboards for academic decision-making**."*

---

### 2.3 Proposed Solution Overview

The **Student Result Management System (SRMS)** shall be a full-stack web application providing:

- A **secure login portal** with role-based access control (Admin, Faculty, Student, Exam Cell Officer, HOD)
- **Automated mark entry** forms for internal assessments and practicals
- **Real-time grade computation** based on configurable university grading scheme (e.g., 10-point CGPA scale)
- **Multi-level approval workflow**: Faculty → HOD → Exam Cell → Publication
- **Instant, secure online result viewing** for students via authenticated dashboard
- **On-demand generation** of mark sheets, grade cards, and transcripts in PDF format
- **Backlog and arrear tracking** module
- **Analytics dashboard** for HOD/Principal showing pass rates, top performers, and course-wise averages
- **Data archiving** and retrieval for historical semester data

---

### 2.4 Process Model Selection

After evaluating available software development process models against the nature of this project, the **Waterfall Model** has been selected as the primary development methodology for the following reasons:

| Criterion | Waterfall Justification |
|---|---|
| **Requirements Stability** | Requirements are well-defined, university-regulated, and unlikely to change mid-development. |
| **Regulatory Compliance** | University grade policies are fixed; the system must conform to documented academic rules. |
| **Documentation** | Waterfall's phase-gate approach produces the mandatory documentation required for university IT procurement. |
| **Team & Timeline** | A structured, sequential plan suits the contracted development team and fixed academic delivery deadline. |
| **Testing & Validation** | Each phase can be verified before proceeding, reducing cumulative rework. |

> **Selected Model: Waterfall**

The development phases are:

1. **Requirements Analysis** — Elicit, document, and freeze all system requirements (this document).
2. **System Design** — Produce architectural diagrams, database schema, and UI wireframes.
3. **Implementation** — Develop the system using the agreed technology stack (web-based, with a relational database).
4. **Testing** — Conduct unit testing, integration testing, user acceptance testing (UAT) with faculty and admin staff.
5. **Deployment** — Host on the university's internal server; train end users.
6. **Maintenance** — Provide post-deployment support and handle semester-based updates.

---

## 3. Stakeholder Analysis

A thorough stakeholder analysis ensures no user group is overlooked during requirements gathering or system design.

| Stakeholder | Role | Interest in System | Level of Influence |
|---|---|---|---|
| **Students** | End beneficiaries of results | View marks, grades, transcripts, backlog status | High |
| **Faculty / Lecturers** | Mark entry and IA administration | Enter internal marks, view course performance | High |
| **Head of Department (HOD)** | Academic oversight | Approve marks, view analytics, monitor programme performance | High |
| **Examination Cell Officer** | ESE marks and official records | Upload ESE marks, generate official result sheets | Very High |
| **University Registrar** | Institutional compliance | Approve final published results, generate academic transcripts | High |
| **Administrative Staff** | Data management support | Assist with data entry, generate printed reports | Medium |
| **IT Department** | System infrastructure | Ensure server availability, manage user accounts, backups | High |
| **Principal / Dean** | Programme governance | Review programme-level analytics and pass rates | Medium |
| **Parents/Guardians** *(optional portal)* | Student outcome visibility | View ward's results via registered email notification | Low |
| **Software Development Company** | System builders | Develop, test, and deliver the system to spec | Very High |

---

## 4. Scope of the Project

### 4.1 In-Scope

The SRMS shall cover the following:

- **Programme:** B.Voc Software Development (Year 1 to Year 3; Semester 1 to Semester 6)
- **Academic Components Managed:**
  - Internal Assessment marks (Test 1, Test 2, Test 3 — best 2 of 3 averaged)
  - Practical/Laboratory marks and records
  - Assignment and project marks
  - Attendance-linked marks (where university policy mandates)
  - End-Semester Examination marks (uploaded by Examination Cell)
  - Final grade calculation and grading scale application
- **System Modules:**
  - User Management & Role-Based Access Control (RBAC)
  - Student Master Data Module
  - Course & Curriculum Management Module
  - Internal Assessment Mark Entry Module
  - ESE Mark Upload & Validation Module
  - Grade Computation Engine
  - Multi-Level Approval Workflow Module
  - Result Publication Module
  - Mark Sheet & Transcript Generation Module
  - Backlog / Arrear Management Module
  - Analytics & Reporting Dashboard
  - Notifications Module (Email / SMS)
  - Data Archiving Module

### 4.2 Out-of-Scope

The following are explicitly excluded from this project:

- Fee management or payment processing
- Attendance marking systems (attendance data may be imported, but attendance capture itself is out of scope)
- Hostel or transportation management
- Library management
- Any other programme or department beyond B.Voc Software Development (unless subsequent phases are approved)
- Mobile native application development (the web application shall be mobile-responsive as a browser-based solution)

---

## 5. System Objectives

The SRMS shall be designed and delivered to achieve the following measurable objectives:

1. **Eliminate Manual Mark Entry Errors** — Implement validation rules and range checks to reduce data-entry errors by ≥ 95% compared to the current manual system.
2. **Accelerate Result Publication** — Reduce the time from last-day-of-examination to published-result from the current average of 21 working days to ≤ 5 working days.
3. **Provide 24/7 Student Access** — Enable students to securely access their marks, grades, and transcripts at any time via the web portal.
4. **Automate Grade Computation** — Apply the university's official CGPA grading formula automatically and consistently across all students and courses, eliminating manual calculation.
5. **Enforce an Accountable Approval Workflow** — Ensure every mark change is audited, timestamped, and attributed to a named user with justification.
6. **Centralise Academic Data** — Establish a single, authoritative database replacing all fragmented Excel sheets and paper registers.
7. **Enable Data-Driven Decisions** — Provide HOD and Principal with dashboards showing programme-level insights: pass rates, course-wise performance, at-risk student identification.
8. **Generate Official Documents On Demand** — Allow the Examination Cell to produce valid mark sheets and transcripts in PDF format within seconds of a request.
9. **Ensure Secure Data Retention** — Archive results for a minimum of 10 years in compliance with university regulations, with role-controlled retrieval.
10. **Support Scalable User Load** — Handle up to 500 concurrent users during peak result-checking periods without performance degradation.

---

## 6. Requirement Analysis

### 6.1 Functional Requirements

Functional requirements describe **what the system must do** — the specific behaviours, functions, and capabilities it must provide.

#### Module 1: User Management & Authentication

| ID | Requirement |
|---|---|
| FR-UM-01 | The system shall support five distinct user roles: Student, Faculty, HOD, Examination Cell Officer, and System Administrator. |
| FR-UM-02 | Each user shall be authenticated via a unique username and a hashed password. |
| FR-UM-03 | The system shall enforce role-based access control so that each role can only access modules and data pertinent to their function. |
| FR-UM-04 | The system shall support password reset via a registered institutional email OTP mechanism. |
| FR-UM-05 | The Administrator shall be able to create, modify, suspend, and delete user accounts. |
| FR-UM-06 | The system shall maintain an activity log of all user logins, logouts, and significant actions. |

#### Module 2: Student Master Data Management

| ID | Requirement |
|---|---|
| FR-SM-01 | The Administrator shall be able to enrol new students by entering: Student ID, Full Name, Date of Birth, Gender, Parent/Guardian Name, Contact Details, Year of Admission, and Programme Batch. |
| FR-SM-02 | The system shall support bulk import of student records via a standardised CSV/Excel file template. |
| FR-SM-03 | Student records shall be editable (with audit trail) by Administrator only; viewable by Faculty, HOD, and the student themselves. |
| FR-SM-04 | The system shall allow a student's academic status to be flagged as: Active, On Leave, Detained (due to low attendance), or Alumni. |
| FR-SM-05 | The system shall store and display the student's complete academic history across all semesters. |

#### Module 3: Course & Curriculum Management

| ID | Requirement |
|---|---|
| FR-CC-01 | The Administrator shall define the curriculum for each semester: Course Code, Course Name, Course Type (Theory/Practical/Project), Credit Hours, Maximum Internal Marks, and Maximum ESE Marks. |
| FR-CC-02 | The system shall store the university's official grading scale (e.g., O, A+, A, B+, B, C, P, F) with corresponding percentage ranges and grade points. |
| FR-CC-03 | Courses shall be assignable to specific faculty members by the Administrator or HOD. |
| FR-CC-04 | The system shall maintain version history when curriculum changes are made (e.g., revised syllabi, added courses). |

#### Module 4: Internal Assessment (IA) Mark Entry

| ID | Requirement |
|---|---|
| FR-IA-01 | Faculty shall be able to enter internal assessment marks for each student in their assigned courses. |
| FR-IA-02 | The system shall support three internal test slots. For calculation purposes, the best two out of three shall be automatically selected by the system. |
| FR-IA-03 | The system shall validate that no mark entered exceeds the defined maximum for that component. |
| FR-IA-04 | Faculty shall be able to save marks as a draft and submit for approval when complete. |
| FR-IA-05 | Once submitted, IA marks shall enter a HOD approval queue and shall be locked for further editing by faculty. |
| FR-IA-06 | The system shall compute the total IA marks for each student per course automatically upon HOD approval. |

#### Module 5: End-Semester Examination (ESE) Mark Management

| ID | Requirement |
|---|---|
| FR-ESE-01 | The Examination Cell Officer shall upload ESE mark data via a validated CSV file or via a structured online input form. |
| FR-ESE-02 | The system shall cross-validate uploaded ESE data against the enrolled student list and flag discrepancies (e.g., missing students, out-of-range values). |
| FR-ESE-03 | ESE marks shall require approval from the Registrar or designated authority before being merged with IA marks for final grade computation. |
| FR-ESE-04 | The system shall prevent ESE data overwriting once approved, except via an explicit override with documented justification. |

#### Module 6: Grade Computation Engine

| ID | Requirement |
|---|---|
| FR-GC-01 | Upon IApproval and ESE approval, the system shall automatically compute each student's total marks per course as: Total = (IA_Obtained / IA_Max × 40) + (ESE_Obtained / ESE_Max × 60). |
| FR-GC-02 | The system shall assign a letter grade and grade point based on the computed total percentage as per the configured grading scale. |
| FR-GC-03 | The system shall compute the Semester Grade Point Average (SGPA) for each student = Σ(Grade Point × Credits) / Σ(Credits). |
| FR-GC-04 | The system shall compute the Cumulative Grade Point Average (CGPA) across all completed semesters. |
| FR-GC-05 | If a student scores below the passing threshold in any course, the system shall automatically flag the course as a backlog and update the student's backlog register. |

#### Module 7: Approval Workflow

| ID | Requirement |
|---|---|
| FR-AW-01 | IA marks submitted by faculty shall be reviewed and approved or returned (with comments) by the HOD. |
| FR-AW-02 | ESE marks uploaded by the Examination Cell shall require approval by the Registrar. |
| FR-AW-03 | Final computed results shall require a final publication approval from the Examination Cell Officer. |
| FR-AW-04 | At each stage, the system shall send an automated email/notification to the next approver in the workflow chain. |
| FR-AW-05 | The system shall maintain a complete timestamped audit trail for every approval action, including the user who approved/rejected, date-time, and any remarks. |

#### Module 8: Result Publication

| ID | Requirement |
|---|---|
| FR-RP-01 | Once fully approved, the Examination Cell Officer shall publish results by clicking a "Publish Results" control. |
| FR-RP-02 | Published results shall be immediately visible to students upon login. |
| FR-RP-03 | The system shall trigger an automated email and/or SMS notification to all students of that semester informing them that results are published. |
| FR-RP-04 | Results, once published, shall be immutable; any correction shall require an explicit, logged re-open request. |

#### Module 9: Mark Sheet & Transcript Generation

| ID | Requirement |
|---|---|
| FR-MS-01 | Students shall be able to download their individual mark sheet for any semester as a PDF document. |
| FR-MS-02 | The Examination Cell shall be able to generate consolidated class mark sheets for all students of a semester/course. |
| FR-MS-03 | The system shall generate an official Cumulative Grade Card (Transcript) for students upon completion of multiple semesters, reflecting all courses and CGPA. |
| FR-MS-04 | Generated mark sheets and transcripts shall bear university branding, the student's photograph (if uploaded), and a unique document reference number for authenticity verification. |

#### Module 10: Backlog & Arrear Management

| ID | Requirement |
|---|---|
| FR-BA-01 | The system shall maintain a dedicated backlog register listing all students with pending arrear examinations, the course(s) concerned, and the number of attempts. |
| FR-BA-02 | When a student clears a backlog, the Examination Cell shall update the system, and the updated CGPA shall be recalculated automatically. |
| FR-BA-03 | The system shall notify the HOD and student when a backlog attempt limit is approaching (configurable). |

#### Module 11: Analytics & Reporting Dashboard

| ID | Requirement |
|---|---|
| FR-AR-01 | The HOD dashboard shall display: total students per semester, overall pass percentage per course, course-wise average marks, and top 10 performers. |
| FR-AR-02 | The system shall identify and flag at-risk students (those with CGPA below a configurable threshold, e.g., CGPA < 5.0). |
| FR-AR-03 | The system shall allow export of all analytical reports as Excel and PDF files. |
| FR-AR-04 | Year-over-year performance comparison reports shall be available for the Principal/Dean view. |

---

### 6.2 Non-Functional Requirements

Non-functional requirements define **how well** the system must perform — its quality attributes.

| Category | ID | Requirement |
|---|---|---|
| **Performance** | NFR-P-01 | The system shall load any student result page within 2 seconds under standard network conditions. |
| **Performance** | NFR-P-02 | The system shall support at least 500 simultaneous authenticated users during peak result-publication periods without performance degradation > 20%. |
| **Performance** | NFR-P-03 | Batch operations (e.g., grade computation for an entire semester cohort of 200 students) shall complete within 30 seconds. |
| **Security** | NFR-S-01 | All data in transit shall be encrypted using HTTPS/TLS 1.2 or higher. |
| **Security** | NFR-S-02 | All passwords shall be stored using a one-way cryptographic hashing algorithm (bcrypt or Argon2). |
| **Security** | NFR-S-03 | The system shall implement session timeout after 15 minutes of inactivity. |
| **Security** | NFR-S-04 | The system shall log all mark modification attempts, including failed ones, for audit purposes. |
| **Security** | NFR-S-05 | Access to a student's personal results shall be restricted exclusively to that student, their assigned faculty, the HOD, and the Examination Cell. |
| **Reliability** | NFR-R-01 | The system shall achieve an uptime of ≥ 99.5% measured monthly, excluding planned maintenance windows. |
| **Reliability** | NFR-R-02 | Automated daily database backups shall be performed and stored in a geographically separate location. |
| **Reliability** | NFR-R-03 | The system shall provide a recovery time objective (RTO) of ≤ 4 hours in the event of a data-centre failure. |
| **Usability** | NFR-U-01 | The interface shall be navigable to a new user within 15 minutes of first use without dedicated training for standard tasks (mark entry, result viewing). |
| **Usability** | NFR-U-02 | The system shall provide inline validation messages with corrective guidance rather than generic error codes. |
| **Usability** | NFR-U-03 | The web interface shall be fully responsive and render correctly on desktop, tablet, and mobile browsers. |
| **Usability** | NFR-U-04 | The system shall support accessibility standards (WCAG 2.1 Level AA). |
| **Maintainability** | NFR-M-01 | The system shall be developed using modular architecture so that individual modules (e.g., grading scheme) can be updated independently. |
| **Maintainability** | NFR-M-02 | The system shall provide an administrative configuration panel for updating grading scales, semester dates, and academic settings without code changes. |
| **Scalability** | NFR-SC-01 | The system architecture shall support horizontal scaling to accommodate the addition of new batches, semesters, or extension to other programmes in the future. |
| **Compliance** | NFR-C-01 | The system shall retain academic data for a minimum of 10 years in compliance with university archival policies. |
| **Compliance** | NFR-C-02 | The system shall comply with applicable data protection and privacy regulations (e.g., Information Technology Act, institutional data governance policies). |

---

### 6.3 Data Flow Diagram (DFD)

#### Level-0 (Context Diagram) — Text Description

The Level-0 DFD represents the entire SRMS as a single process interacting with its external entities.

```
[Student]              ──(Login credentials, mark view request)──────────► [SRMS]
[SRMS]                 ──(Published results, mark sheets, notifications)───► [Student]

[Faculty]              ──(Login credentials, IA mark data)────────────────► [SRMS]
[SRMS]                 ──(Mark entry confirmation, course assignments)─────► [Faculty]

[HOD]                  ──(Login credentials, approval/rejection decision)──► [SRMS]
[SRMS]                 ──(Pending approval lists, analytics reports)───────► [HOD]

[Examination Cell]     ──(ESE mark uploads, approval decisions)───────────► [SRMS]
[SRMS]                 ──(Consolidated mark sheets, result status)─────────► [Examination Cell]

[Administrator]        ──(User/course/programme configuration data)────────► [SRMS]
[SRMS]                 ──(Confirmation, audit logs)───────────────────────► [Administrator]

[SRMS]  ◄──────────────────────────────────────────────────────────────────► [Students DB]
[SRMS]  ◄──────────────────────────────────────────────────────────────────► [Courses DB]
[SRMS]  ◄──────────────────────────────────────────────────────────────────► [Marks DB]
[SRMS]  ◄──────────────────────────────────────────────────────────────────► [Results DB]
[SRMS]  ◄──────────────────────────────────────────────────────────────────► [Users DB]
[SRMS]  ──(Email/SMS notifications)──────────────────────────────────────► [Notification Service]
```

> *Refer to Figure 1 (attached diagram) for the graphical Level-0 DFD. The textual description above maps exactly to that figure.*

---

#### Level-1 DFD — Sub-Processes Breakdown

The main SRMS process is decomposed into the following Level-1 sub-processes:

| Process ID | Process Name | Input Data Flows | Output Data Flows | Data Stores Accessed |
|---|---|---|---|---|
| **P1** | Authenticate User | Login credentials | Auth token / Error message | Users DB |
| **P2** | Manage Student Data | Student enrolment data | Confirmation | Students DB |
| **P3** | Manage Courses | Course definitions | Course list | Courses DB |
| **P4** | Enter IA Marks | IA mark data (by Faculty) | Draft/submitted marks | Marks DB |
| **P5** | Upload ESE Marks | ESE mark file (by Exam Cell) | Validated mark set | Marks DB |
| **P6** | Approve Marks | Approval/rejection decision | Status update, notification | Marks DB, Users DB |
| **P7** | Compute Grades | Approved IA + ESE marks | Grade, SGPA, CGPA | Results DB, Marks DB |
| **P8** | Publish Results | Publish command | Published result flags + notifications | Results DB |
| **P9** | Generate Documents | Document request | PDF mark sheet / transcript | Results DB, Students DB |
| **P10** | Report & Analytics | Query parameters | Charts, tables, exports | Results DB, Marks DB |

---

### 6.4 Data Dictionary

The data dictionary defines all critical data items used within the SRMS.

#### Table: `students`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `student_id` | VARCHAR | 12 | PRIMARY KEY, NOT NULL, UNIQUE | University-assigned unique student identifier | `BVOC2024001` |
| `full_name` | VARCHAR | 150 | NOT NULL | Student's full legal name | `Priya Sharma` |
| `date_of_birth` | DATE | — | NOT NULL | Student's date of birth | `2005-08-15` |
| `gender` | CHAR | 1 | NOT NULL, CHECK (M/F/O) | Gender code | `F` |
| `email` | VARCHAR | 150 | NOT NULL, UNIQUE | Institutional email address | `priya.sharma@univ.edu.in` |
| `phone` | VARCHAR | 15 | NOT NULL | Contact phone number | `9876543210` |
| `batch_year` | INTEGER | 4 | NOT NULL | Year of programme admission | `2024` |
| `current_semester` | INTEGER | 1 | NOT NULL, CHECK (1–6) | Current active semester | `2` |
| `status` | VARCHAR | 20 | NOT NULL, DEFAULT 'Active' | Enrolment status | `Active` |
| `photo_url` | VARCHAR | 255 | NULLABLE | Path to student photograph | `/uploads/students/BVOC2024001.jpg` |
| `guardian_name` | VARCHAR | 150 | NOT NULL | Parent/Guardian name | `Ramesh Sharma` |
| `date_enrolled` | DATE | — | NOT NULL | Date of university enrolment | `2024-07-01` |

#### Table: `courses`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `course_code` | VARCHAR | 10 | PRIMARY KEY, NOT NULL, UNIQUE | University course code | `BVSD201` |
| `course_name` | VARCHAR | 200 | NOT NULL | Full name of the course | `Data Structures and Algorithms` |
| `semester` | INTEGER | 1 | NOT NULL, CHECK (1–6) | Semester in which course is taught | `2` |
| `course_type` | VARCHAR | 20 | NOT NULL | Theory, Practical, or Project | `Theory` |
| `credit_hours` | INTEGER | 2 | NOT NULL | Credit units assigned | `4` |
| `max_ia_marks` | INTEGER | 3 | NOT NULL | Maximum internal assessment marks | `40` |
| `max_ese_marks` | INTEGER | 3 | NOT NULL | Maximum end-semester exam marks | `60` |
| `faculty_id` | INTEGER | 10 | FOREIGN KEY → `faculty.faculty_id` | Assigned faculty member | `1012` |

#### Table: `faculty`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `faculty_id` | INTEGER | 10 | PRIMARY KEY, NOT NULL | Unique faculty identifier | `1012` |
| `name` | VARCHAR | 150 | NOT NULL | Faculty member's name | `Dr. Anil Mehta` |
| `department` | VARCHAR | 100 | NOT NULL | Department | `Software Development` |
| `email` | VARCHAR | 150 | NOT NULL, UNIQUE | Institutional email | `a.mehta@univ.edu.in` |
| `designation` | VARCHAR | 100 | NOT NULL | Academic designation | `Assistant Professor` |

#### Table: `ia_marks`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `ia_id` | INTEGER | 10 | PRIMARY KEY, AUTO_INCREMENT | Unique IA mark entry ID | `5001` |
| `student_id` | VARCHAR | 12 | FOREIGN KEY → `students.student_id` | Student concerned | `BVOC2024001` |
| `course_code` | VARCHAR | 10 | FOREIGN KEY → `courses.course_code` | Course concerned | `BVSD201` |
| `semester` | INTEGER | 1 | NOT NULL | Semester of this entry | `2` |
| `test1_marks` | DECIMAL | 5,2 | NULLABLE | Marks in Internal Test 1 | `17.50` |
| `test2_marks` | DECIMAL | 5,2 | NULLABLE | Marks in Internal Test 2 | `19.00` |
| `test3_marks` | DECIMAL | 5,2 | NULLABLE | Marks in Internal Test 3 | `15.00` |
| `best_two_avg` | DECIMAL | 5,2 | COMPUTED | Average of best 2 test marks | `18.25` |
| `practical_marks` | DECIMAL | 5,2 | NULLABLE | Practical/lab marks | `12.00` |
| `assignment_marks` | DECIMAL | 5,2 | NULLABLE | Assignment marks | `8.00` |
| `total_ia` | DECIMAL | 5,2 | COMPUTED | Total internal marks | `38.25` |
| `status` | VARCHAR | 20 | NOT NULL, DEFAULT 'Draft' | Draft / Submitted / Approved | `Approved` |
| `entered_by` | INTEGER | 10 | FOREIGN KEY → `faculty.faculty_id` | Faculty who entered marks | `1012` |
| `approved_by` | INTEGER | 10 | NULLABLE, FOREIGN KEY → `users.user_id` | HOD who approved | `2001` |
| `approved_at` | DATETIME | — | NULLABLE | Timestamp of HOD approval | `2025-11-30 14:32:00` |

#### Table: `ese_marks`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `ese_id` | INTEGER | 10 | PRIMARY KEY, AUTO_INCREMENT | Unique ESE mark entry ID | `8001` |
| `student_id` | VARCHAR | 12 | FOREIGN KEY → `students.student_id` | Student concerned | `BVOC2024001` |
| `course_code` | VARCHAR | 10 | FOREIGN KEY → `courses.course_code` | Course concerned | `BVSD201` |
| `semester` | INTEGER | 1 | NOT NULL | Semester of this entry | `2` |
| `ese_marks_obtained` | DECIMAL | 5,2 | NOT NULL | Marks obtained in ESE | `47.50` |
| `is_absent` | BOOLEAN | — | DEFAULT FALSE | Whether student was absent | `FALSE` |
| `uploaded_by` | INTEGER | 10 | FOREIGN KEY → `users.user_id` | Examination Cell Officer | `3001` |
| `approved_by` | INTEGER | 10 | NULLABLE | Registrar who approved | `4001` |
| `approved_at` | DATETIME | — | NULLABLE | Timestamp of approval | `2025-12-15 09:00:00` |

#### Table: `results`

| Data Item | Data Type | Length / Precision | Constraints | Description | Example Value |
|---|---|---|---|---|---|
| `result_id` | INTEGER | 10 | PRIMARY KEY, AUTO_INCREMENT | Unique result record ID | `10001` |
| `student_id` | VARCHAR | 12 | FOREIGN KEY → `students.student_id` | Student | `BVOC2024001` |
| `course_code` | VARCHAR | 10 | FOREIGN KEY → `courses.course_code` | Course | `BVSD201` |
| `semester` | INTEGER | 1 | NOT NULL | Semester | `2` |
| `total_marks` | DECIMAL | 5,2 | NOT NULL | Computed total (out of 100) | `72.50` |
| `letter_grade` | CHAR | 3 | NOT NULL | Assigned letter grade | `A` |
| `grade_point` | DECIMAL | 3,1 | NOT NULL | Grade point for CGPA calc | `8.0` |
| `is_pass` | BOOLEAN | — | NOT NULL | True if student passed | `TRUE` |
| `is_backlog` | BOOLEAN | — | DEFAULT FALSE | True if course is a backlog | `FALSE` |
| `sgpa` | DECIMAL | 4,2 | NULLABLE | Semester GPA (on result record for semester-level) | `7.85` |
| `published` | BOOLEAN | — | DEFAULT FALSE | Whether result is published | `TRUE` |
| `published_at` | DATETIME | — | NULLABLE | Result publication timestamp | `2025-12-20 10:00:00` |

---

### 6.5 Use Case Diagram & Descriptions

#### Actors

- **Student** — Views results, downloads mark sheets and transcripts.
- **Faculty** — Enters and submits internal assessment marks.
- **HOD** — Approves/rejects IA marks, views department analytics.
- **Examination Cell Officer (ECO)** — Uploads ESE marks, publishes results, generates consolidated documents.
- **Administrator (Admin)** — Manages users, courses, programme configuration.
- **System (Automated)** — Sends notifications, computes grades, archives data.

#### Use Case Summary Table

| Actor | Use Cases |
|---|---|
| **Student** | Login, View Marks, View Grade Card, Download Mark Sheet, Download Transcript, View Backlog Status, Logout |
| **Faculty** | Login, Enter IA Marks (Draft), Submit IA Marks for Approval, View Submitted Mark Status, Logout |
| **HOD** | Login, View Pending Approval Queue, Approve IA Marks, Return Marks to Faculty, View Analytics Dashboard, Export Reports |
| **ECO** | Login, Upload ESE Marks, Validate ESE Data, Request ESE Approval, Publish Results, Generate Consolidated Mark Sheets |
| **Admin** | Manage Users, Manage Student Records (CRUD), Manage Courses, Configure Grading Scale, View Audit Logs |
| **System** | Send Approval Notifications, Compute Final Grades, Auto-flag Backlogs, Send Result Publication Notifications |

---

#### Use Case Description 1 — Enter Internal Assessment Marks

| Element | Description |
|---|---|
| **Use Case Name** | Enter Internal Assessment (IA) Marks |
| **Use Case ID** | UC-04 |
| **Actor** | Faculty |
| **Precondition** | Faculty is logged in. Courses are assigned to this faculty member. The current semester IA mark-entry window is open (period activated by Administrator). |
| **Main Flow** | 1. Faculty selects the "IA Mark Entry" module from the dashboard. <br>2. System displays the list of courses assigned to this faculty for the active semester. <br>3. Faculty selects a course. <br>4. System displays a mark-entry grid listing all enrolled students with input fields for Test 1, Test 2, Test 3, Practical, and Assignment marks. <br>5. Faculty enters marks for each student. <br>6. System validates in real-time: marks must be numeric and ≤ maximum defined for that component. <br>7. Faculty saves the entry as **Draft**. System stores data without forwarding for approval. <br>8. When complete, Faculty clicks **Submit for Approval**. <br>9. System locks the mark sheet, updates status to "Submitted", and sends an automated notification to the HOD. |
| **Alternative Flow** | - *If a mark exceeds the maximum:* System highlights the field in red and shows "Entered value exceeds maximum allowed (X). Please correct." Faculty cannot submit until all errors are resolved. <br>- *If the mark-entry window is closed:* System displays "Mark entry period has ended. Contact Administrator." |
| **Postcondition** | IA marks for the selected course and semester are saved and submitted; HOD notification has been triggered; marks are locked for faculty editing. |

---

#### Use Case Description 2 — Approve IA Marks (HOD)

| Element | Description |
|---|---|
| **Use Case Name** | Approve Internal Assessment Marks |
| **Use Case ID** | UC-06 |
| **Actor** | HOD |
| **Precondition** | HOD is logged in. At least one IA mark submission is pending approval from a faculty member. |
| **Main Flow** | 1. HOD navigates to the **Approvals** section of the dashboard. <br>2. System displays a list of pending mark submissions grouped by course and faculty. <br>3. HOD selects a pending submission. <br>4. System displays the full mark sheet for review. <br>5. HOD reviews marks and either: <br>&nbsp;&nbsp;&nbsp;**a. Approves:** Clicks "Approve." System updates status to "Approved," triggers the grade computation pipeline, and notifies the faculty. <br>&nbsp;&nbsp;&nbsp;**b. Returns with Comments:** Clicks "Return," enters remarks (e.g., "Test 3 marks for student BVOC2024003 seem incorrect — please verify"). System unlocks the marks for faculty correction and notifies faculty. |
| **Alternative Flow** | - *If HOD approves marks that contain outlier values (e.g., all students scored 0):* System displays a warning "This submission contains anomalous values. Do you wish to proceed?" HOD must confirm. <br>- *If faculty has not yet submitted:* The course does not appear in the approval queue. |
| **Postcondition** | Approved mark set is locked; grade computation sub-process is triggered for the affected course-semester cohort; faculty receives approval notification. |

---

#### Use Case Description 3 — Publish Results

| Element | Description |
|---|---|
| **Use Case Name** | Publish Semester Results |
| **Use Case ID** | UC-08 |
| **Actor** | Examination Cell Officer |
| **Precondition** | ECO is logged in. All IA marks for the semester are approved. All ESE marks are uploaded and approved by the Registrar. Grade computation has completed successfully. |
| **Main Flow** | 1. ECO navigates to the **Result Management → Publish Results** panel. <br>2. System displays a pre-publication checklist: IA Approval Status, ESE Upload Status, ESE Approval Status, Grade Computation Status — all must show "Complete." <br>3. ECO reviews the checklist and confirms all are marked complete. <br>4. ECO clicks **Publish Results**. <br>5. System displays a confirmation dialogue: "You are about to publish results for Semester [X] Batch [YYYY]. This action is final. Proceed?" <br>6. ECO confirms. <br>7. System sets `published = TRUE` and `published_at = NOW()` for all result records of the semester. <br>8. System triggers automated email/SMS notifications to all students of the semester. <br>9. Results become visible on student dashboards immediately. |
| **Alternative Flow** | - *If any checklist item is incomplete:* The "Publish Results" button remains disabled. System shows "Cannot publish: ESE marks not yet approved." <br>- *If ECO wishes to cancel:* They click "Cancel" on the confirmation dialogue and no action is taken. |
| **Postcondition** | Results are published and immutable; students receive notifications; result publication event is recorded in the audit log. |

---

#### Use Case Description 4 — Download Mark Sheet (Student)

| Element | Description |
|---|---|
| **Use Case Name** | Download Semester Mark Sheet |
| **Use Case ID** | UC-11 |
| **Actor** | Student |
| **Precondition** | Student is logged in. Results for the requested semester are published. |
| **Main Flow** | 1. Student navigates to **My Results → Semester [X]**. <br>2. System displays the result summary: list of courses, marks, grades, SGPA. <br>3. Student clicks **Download Mark Sheet (PDF)**. <br>4. System generates a PDF document containing: University logo and name, Student name and ID, batch details, course-wise marks and grades, SGPA, HOD/Registrar digital signature fields, and a unique document reference number. <br>5. PDF is downloaded to the student's device. |
| **Alternative Flow** | - *If results are not yet published:* Student sees "Results for this semester have not been published yet." No download option is shown. <br>- *If the student has an active backlog:* A note is included in the mark sheet: "One or more courses are pending clearance." |
| **Postcondition** | Student has a PDF copy of the mark sheet; a download event is logged. |

---

## 7. Project Management

### 7.1 Function Point Analysis

Function Point Analysis (FPA) measures the software's functional size based on user-visible operations, independent of the programming language or technology used.

#### Complexity Weights Used

| Function Type | Simple | Average | Complex |
|---|---|---|---|
| External Input (EI) | 3 | 4 | 6 |
| External Output (EO) | 4 | 5 | 7 |
| External Query (EQ) | 3 | 4 | 6 |
| Internal Logical File (ILF) | 7 | 10 | 15 |
| External Interface File (EIF) | 5 | 7 | 10 |

#### Function Point Count Table

| Function Type | Description | Complexity | Weight | Count | Contribution |
|---|---|---|---|---|---|
| **External Inputs (EI)** | Add/Edit Student Record | Average | 4 | 1 | 4 |
| | Bulk Import Students (CSV) | Complex | 6 | 1 | 6 |
| | Enter IA Marks (per course) | Average | 4 | 1 | 4 |
| | Upload ESE Marks (CSV) | Complex | 6 | 1 | 6 |
| | Submit IA Marks for Approval | Simple | 3 | 1 | 3 |
| | Approve / Return IA Marks | Average | 4 | 1 | 4 |
| | Approve ESE Marks | Average | 4 | 1 | 4 |
| | Publish Results | Average | 4 | 1 | 4 |
| | Configure Grading Scale | Average | 4 | 1 | 4 |
| | Add/Edit Course Definition | Average | 4 | 1 | 4 |
| | Create / Manage User Account | Average | 4 | 1 | 4 |
| | Update Backlog Status | Simple | 3 | 1 | 3 |
| | **EI Sub-total** | | | **12** | **50** |
| **External Outputs (EO)** | PDF Student Mark Sheet | Complex | 7 | 1 | 7 |
| | PDF Cumulative Transcript | Complex | 7 | 1 | 7 |
| | Consolidated Class Mark Sheet | Complex | 7 | 1 | 7 |
| | Email/SMS Result Notification | Simple | 4 | 1 | 4 |
| | Analytics Export (Excel/PDF) | Average | 5 | 1 | 5 |
| | **EO Sub-total** | | | **5** | **30** |
| **External Queries (EQ)** | View Individual Student Results | Average | 4 | 1 | 4 |
| | Search Student Records | Average | 4 | 1 | 4 |
| | View Course Mark List by Faculty | Average | 4 | 1 | 4 |
| | View HOD Analytics Dashboard | Complex | 6 | 1 | 6 |
| | View Backlog Register | Average | 4 | 1 | 4 |
| | View Audit Logs | Average | 4 | 1 | 4 |
| | View Approval Queue | Simple | 3 | 1 | 3 |
| | **EQ Sub-total** | | | **7** | **29** |
| **Internal Logical Files (ILF)** | Students Table | Average | 10 | 1 | 10 |
| | Courses Table | Average | 10 | 1 | 10 |
| | Faculty Table | Simple | 7 | 1 | 7 |
| | IA Marks Table | Average | 10 | 1 | 10 |
| | ESE Marks Table | Average | 10 | 1 | 10 |
| | Results Table | Average | 10 | 1 | 10 |
| | Users / Roles Table | Simple | 7 | 1 | 7 |
| | Audit Log Table | Simple | 7 | 1 | 7 |
| | Notifications Table | Simple | 7 | 1 | 7 |
| | **ILF Sub-total** | | | **9** | **78** |
| **External Interface Files (EIF)** | Email / SMS Notification Gateway | Average | 7 | 1 | 7 |
| | **EIF Sub-total** | | | **1** | **7** |
| **Total Unadjusted Function Points (UFP)** | | | | | **194** |

---

### 7.2 Effort Estimation

Using the function point count, effort is estimated as follows:

**Formula:** `Effort (person-hours) = UFP × Hours per FP`

Given that this is a moderately complex, domain-specific system using standard web technologies (e.g., Node.js / Python Django with PostgreSQL), a productivity factor of **3 hours per FP** is applied.

```
Estimated Effort = 194 × 3 = 582 person-hours
```

**Team Composition:** Assuming a team of 4 developers (1 Project Manager/Lead, 2 Full-Stack Developers, 1 QA Engineer):

```
Parallel working hours = 582 / 4 = ~145.5 hours per developer
Working at 8 hours/day, 5 days/week = ~18.2 working days ≈ 4 weeks of pure coding
```

**Accounting for design, testing, UAT, and deployment (multiplier of ~2.5x):**

```
Total Calendar Duration ≈ 582 × 2.5 / (4 × 8 × 5) = 9.1 weeks ≈ 10 weeks (2.5 months)
```

> **Summary:** Based on Function Point Analysis (UFP = 194) and a productivity factor of 3 hours/FP, the estimated total development effort is approximately **582 person-hours**. With a team of 4 professionals working in parallel and accounting for all phases, the projected delivery timeline is **10–12 weeks** from project kick-off.

---

### 7.3 Project Schedule & Gantt Overview

| Phase | Tasks | Duration | Responsible |
|---|---|---|---|
| **Phase 0: Initiation** | Requirements sign-off, team setup, environment setup | Week 1 | PM, All |
| **Phase 1: Design** | Architecture design, database schema, UI wireframes, review | Weeks 2–3 | Lead Dev, PM |
| **Phase 2: Implementation – Core** | User Auth, Student & Course modules, IA Mark Entry | Weeks 4–6 | Dev 1, Dev 2 |
| **Phase 3: Implementation – Advanced** | ESE Upload, Grade Engine, Approval Workflow, Result Publication | Weeks 6–8 | Dev 1, Dev 2 |
| **Phase 4: Implementation – Reporting** | Mark Sheet/Transcript PDF generation, Analytics Dashboard | Weeks 8–9 | Dev 2, Dev 1 |
| **Phase 5: Testing** | Unit testing, Integration testing, Security testing | Weeks 9–10 | QA Engineer |
| **Phase 6: UAT** | User acceptance testing with actual faculty, HOD, Exam Cell | Week 10–11 | QA, PM, Stakeholders |
| **Phase 7: Deployment** | Production deployment, data migration, user training | Week 11–12 | PM, Dev 1, IT |
| **Phase 8: Warranty** | Post-deployment support, bug fixes | Weeks 13–16 | All |

---

### 7.4 Risk Table

| Risk ID | Risk Description | Probability | Impact | Risk Level | Mitigation Strategy |
|---|---|---|---|---|---|
| **R-01** | University-defined grading rules change mid-development | Medium | High | **High** | Freeze grading configuration in Phase 0; implement configurable grade scale module to accommodate future changes without code changes. |
| **R-02** | Faculty resistance to digital mark entry (adoption risk) | Medium | High | **High** | Conduct pre-launch training sessions; provide a simple, intuitive UI; designate IT champions per department. |
| **R-03** | ESE mark data received from examination cell in inconsistent format | High | Medium | **High** | Define a strict CSV import template in Phase 0; build a robust validation and error-reporting layer in the ESE upload module. |
| **R-04** | Performance degradation during simultaneous result access (peak load) | Medium | High | **High** | Load test with 500 concurrent users before go-live; implement CDN caching for static assets; use database read replicas. |
| **R-05** | Data privacy breach — unauthorised access to student marks | Low | Very High | **High** | Enforce RBAC strictly; encrypt all data in transit (TLS); encrypt sensitive fields at rest; regular penetration testing. |
| **R-06** | Scope creep — university requests additional features mid-project | High | Medium | **Medium** | Strictly follow the requirements signed in Phase 0; all new requests to be logged and deferred to Phase 2 (future version). |
| **R-07** | Key developer unavailability (illness or attrition) | Low | High | **Medium** | Maintain shared code repository (Git); enforce code review and documentation; adopt pair-programming for critical modules. |
| **R-08** | Server/infrastructure unavailability during peak result period | Low | Very High | **High** | Negotiate a guaranteed uptime SLA with IT; schedule planned maintenance outside academic calendars. |
| **R-09** | Inaccurate student data in initial import | Medium | Medium | **Medium** | Design and provide a student data entry template; validate all imported data against university register before go-live. |
| **R-10** | PDF generation library licensing or compatibility issues | Low | Low | **Low** | Select a well-supported, open-source library (e.g., WeasyPrint, ReportLab, or iText) during Phase 1; test early. |

---

## 8. Design Engineering

### 8.1 Architectural Design

The SRMS shall be built on a **Three-Tier (Layered) Architecture**, ensuring clean separation of concerns, ease of maintenance, and scalability.

```
┌─────────────────────────────────────────────────────────┐
│                PRESENTATION LAYER                        │
│         (Responsive Web Application - Browser)           │
│  ┌─────────────┐  ┌────────────┐  ┌────────────────────┐ │
│  │ Student     │  │ Faculty    │  │ HOD / Admin /      │ │
│  │ Dashboard   │  │ Portal     │  │ Exam Cell Portal   │ │
│  └─────────────┘  └────────────┘  └────────────────────┘ │
└─────────────────────────┬───────────────────────────────┘
                          │  HTTPS / REST API (JSON)
┌─────────────────────────▼───────────────────────────────┐
│               BUSINESS LOGIC LAYER                       │
│              (Application Server - API)                  │
│  ┌──────────┐ ┌───────────┐ ┌──────────┐ ┌───────────┐  │
│  │Auth &    │ │Mark Entry │ │Grade     │ │Document   │  │
│  │RBAC      │ │& Approval │ │Computation│ │Generation │  │
│  │Module    │ │Workflow   │ │Engine    │ │Engine     │  │
│  └──────────┘ └───────────┘ └──────────┘ └───────────┘  │
│  ┌──────────┐ ┌───────────┐ ┌──────────┐                │
│  │Analytics │ │Notification│ │Audit    │                │
│  │Module    │ │Service    │ │Logger   │                │
│  └──────────┘ └───────────┘ └──────────┘                │
└─────────────────────────┬───────────────────────────────┘
                          │  ORM / Parameterized SQL
┌─────────────────────────▼───────────────────────────────┐
│                  DATA ACCESS LAYER                       │
│            (Repository / DAO Pattern)                    │
│   StudentRepository | CourseRepository | MarkRepository  │
│   ResultRepository  | UserRepository   | AuditRepository │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│                  PERSISTENCE LAYER                       │
│              PostgreSQL Relational Database              │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌───────────┐  │
│  │students  │ │courses   │ │ia_marks  │ │ese_marks  │  │
│  │faculty   │ │users     │ │results   │ │audit_logs │  │
│  └──────────┘ └──────────┘ └──────────┘ └───────────┘  │
└─────────────────────────────────────────────────────────┘
                          │
          ┌───────────────┴───────────────┐
          │    External Services          │
          │  (SMTP / SMS Gateway)         │
          └───────────────────────────────┘
```

**Technology Stack Recommendation:**

| Layer | Recommended Technology |
|---|---|
| **Frontend** | React.js (with TypeScript) + Tailwind CSS |
| **Backend API** | Node.js with Express.js (or Python with Django REST Framework) |
| **Database** | PostgreSQL 15+ |
| **PDF Generation** | PDFKit (Node) or WeasyPrint (Python) |
| **Authentication** | JWT (JSON Web Tokens) with bcrypt password hashing |
| **Hosting** | University's on-premise Linux server (or cloud: AWS / Azure) |
| **Version Control** | Git with GitHub/GitLab |
| **Email/SMS** | SMTP relay (internal university mail server) + SMS gateway API |

---

### 8.2 Data Design (Database Schema)

```sql
-- ============================================================
--  STUDENT RESULT MANAGEMENT SYSTEM (SRMS)
--  Database Schema — PostgreSQL 15+
-- ============================================================

-- Users & Authentication
CREATE TABLE roles (
    role_id     SERIAL PRIMARY KEY,
    role_name   VARCHAR(50) NOT NULL UNIQUE  -- Student, Faculty, HOD, ECO, Admin
);

CREATE TABLE users (
    user_id         SERIAL PRIMARY KEY,
    username        VARCHAR(100) NOT NULL UNIQUE,
    password_hash   VARCHAR(255) NOT NULL,
    role_id         INTEGER NOT NULL REFERENCES roles(role_id),
    email           VARCHAR(150) NOT NULL UNIQUE,
    is_active       BOOLEAN DEFAULT TRUE,
    last_login      TIMESTAMP,
    created_at      TIMESTAMP DEFAULT NOW()
);

-- Student Master
CREATE TABLE students (
    student_id      VARCHAR(12) PRIMARY KEY,          -- e.g., BVOC2024001
    full_name       VARCHAR(150) NOT NULL,
    date_of_birth   DATE NOT NULL,
    gender          CHAR(1) NOT NULL CHECK (gender IN ('M','F','O')),
    email           VARCHAR(150) NOT NULL UNIQUE,
    phone           VARCHAR(15) NOT NULL,
    batch_year      INTEGER NOT NULL,
    current_semester INTEGER NOT NULL CHECK (current_semester BETWEEN 1 AND 6),
    status          VARCHAR(20) NOT NULL DEFAULT 'Active'
                        CHECK (status IN ('Active','On Leave','Detained','Alumni')),
    guardian_name   VARCHAR(150) NOT NULL,
    photo_url       VARCHAR(255),
    user_id         INTEGER UNIQUE REFERENCES users(user_id),
    date_enrolled   DATE NOT NULL,
    created_at      TIMESTAMP DEFAULT NOW()
);

-- Faculty
CREATE TABLE faculty (
    faculty_id      SERIAL PRIMARY KEY,
    name            VARCHAR(150) NOT NULL,
    department      VARCHAR(100) NOT NULL,
    email           VARCHAR(150) NOT NULL UNIQUE,
    designation     VARCHAR(100) NOT NULL,
    user_id         INTEGER UNIQUE REFERENCES users(user_id),
    is_hod          BOOLEAN DEFAULT FALSE
);

-- Courses / Curriculum
CREATE TABLE courses (
    course_code     VARCHAR(10) PRIMARY KEY,           -- e.g., BVSD201
    course_name     VARCHAR(200) NOT NULL,
    semester        INTEGER NOT NULL CHECK (semester BETWEEN 1 AND 6),
    course_type     VARCHAR(20) NOT NULL
                        CHECK (course_type IN ('Theory','Practical','Project')),
    credit_hours    INTEGER NOT NULL,
    max_ia_marks    DECIMAL(5,2) NOT NULL DEFAULT 40.00,
    max_ese_marks   DECIMAL(5,2) NOT NULL DEFAULT 60.00,
    faculty_id      INTEGER REFERENCES faculty(faculty_id),
    is_active       BOOLEAN DEFAULT TRUE
);

-- IA Marks
CREATE TABLE ia_marks (
    ia_id           SERIAL PRIMARY KEY,
    student_id      VARCHAR(12) NOT NULL REFERENCES students(student_id),
    course_code     VARCHAR(10) NOT NULL REFERENCES courses(course_code),
    semester        INTEGER NOT NULL,
    academic_year   VARCHAR(9) NOT NULL,               -- e.g., 2025-2026
    test1_marks     DECIMAL(5,2),
    test2_marks     DECIMAL(5,2),
    test3_marks     DECIMAL(5,2),
    best_two_avg    DECIMAL(5,2) GENERATED ALWAYS AS (
                        CASE
                            WHEN test1_marks IS NOT NULL AND test2_marks IS NOT NULL AND test3_marks IS NOT NULL
                            THEN (test1_marks + test2_marks + test3_marks
                                  - LEAST(test1_marks, test2_marks, test3_marks)) / 2.0
                            ELSE COALESCE((test1_marks + test2_marks) / 2.0,
                                         (test1_marks + test3_marks) / 2.0,
                                         (test2_marks + test3_marks) / 2.0,
                                         COALESCE(test1_marks, test2_marks, test3_marks))
                        END
                    ) STORED,
    practical_marks DECIMAL(5,2) DEFAULT 0,
    assignment_marks DECIMAL(5,2) DEFAULT 0,
    total_ia        DECIMAL(5,2),                      -- computed by application layer
    status          VARCHAR(20) NOT NULL DEFAULT 'Draft'
                        CHECK (status IN ('Draft','Submitted','Approved','Returned')),
    entered_by      INTEGER NOT NULL REFERENCES faculty(faculty_id),
    submitted_at    TIMESTAMP,
    approved_by     INTEGER REFERENCES users(user_id),
    approved_at     TIMESTAMP,
    hod_remarks     TEXT,
    UNIQUE (student_id, course_code, semester, academic_year)
);

-- ESE Marks
CREATE TABLE ese_marks (
    ese_id              SERIAL PRIMARY KEY,
    student_id          VARCHAR(12) NOT NULL REFERENCES students(student_id),
    course_code         VARCHAR(10) NOT NULL REFERENCES courses(course_code),
    semester            INTEGER NOT NULL,
    academic_year       VARCHAR(9) NOT NULL,
    ese_marks_obtained  DECIMAL(5,2) NOT NULL DEFAULT 0,
    is_absent           BOOLEAN DEFAULT FALSE,
    uploaded_by         INTEGER NOT NULL REFERENCES users(user_id),
    uploaded_at         TIMESTAMP DEFAULT NOW(),
    approved_by         INTEGER REFERENCES users(user_id),
    approved_at         TIMESTAMP,
    UNIQUE (student_id, course_code, semester, academic_year)
);

-- Grading Scale
CREATE TABLE grading_scale (
    grade_id        SERIAL PRIMARY KEY,
    letter_grade    VARCHAR(3) NOT NULL UNIQUE,        -- O, A+, A, B+, B, C, P, F
    min_percentage  DECIMAL(5,2) NOT NULL,
    max_percentage  DECIMAL(5,2) NOT NULL,
    grade_point     DECIMAL(3,1) NOT NULL,
    is_pass         BOOLEAN NOT NULL DEFAULT TRUE
);

-- Results (Computed)
CREATE TABLE results (
    result_id       SERIAL PRIMARY KEY,
    student_id      VARCHAR(12) NOT NULL REFERENCES students(student_id),
    course_code     VARCHAR(10) NOT NULL REFERENCES courses(course_code),
    semester        INTEGER NOT NULL,
    academic_year   VARCHAR(9) NOT NULL,
    total_marks     DECIMAL(5,2) NOT NULL,
    letter_grade    VARCHAR(3) NOT NULL,
    grade_point     DECIMAL(3,1) NOT NULL,
    is_pass         BOOLEAN NOT NULL,
    is_backlog      BOOLEAN DEFAULT FALSE,
    sgpa            DECIMAL(4,2),
    cgpa            DECIMAL(4,2),
    published       BOOLEAN DEFAULT FALSE,
    published_by    INTEGER REFERENCES users(user_id),
    published_at    TIMESTAMP,
    UNIQUE (student_id, course_code, semester, academic_year)
);

-- Audit Log
CREATE TABLE audit_log (
    log_id          SERIAL PRIMARY KEY,
    user_id         INTEGER REFERENCES users(user_id),
    action          VARCHAR(100) NOT NULL,
    entity_type     VARCHAR(50),                       -- 'ia_marks', 'ese_marks', 'result', etc.
    entity_id       VARCHAR(50),
    old_value       TEXT,
    new_value       TEXT,
    ip_address      VARCHAR(45),
    logged_at       TIMESTAMP DEFAULT NOW()
);

-- Notifications
CREATE TABLE notifications (
    notif_id        SERIAL PRIMARY KEY,
    recipient_user_id INTEGER REFERENCES users(user_id),
    notif_type      VARCHAR(50) NOT NULL,              -- 'approval_request', 'result_published', etc.
    message         TEXT NOT NULL,
    is_read         BOOLEAN DEFAULT FALSE,
    sent_at         TIMESTAMP DEFAULT NOW()
);
```

---

### 8.3 Component-Level Design (Pseudocode)

#### Component 1: `compute_final_grade(student_id, course_code, semester, academic_year)`

```
function compute_final_grade(student_id, course_code, semester, academic_year):

    # Step 1: Fetch approved IA marks
    ia = query ia_marks
         WHERE student_id = student_id
           AND course_code = course_code
           AND semester    = semester
           AND academic_year = academic_year
           AND status = 'Approved'

    if ia is NULL:
        return ERROR "IA marks not found or not approved for this entry."

    # Step 2: Fetch approved ESE marks
    ese = query ese_marks
          WHERE student_id  = student_id
            AND course_code = course_code
            AND semester    = semester
            AND academic_year = academic_year
            AND approved_by IS NOT NULL

    if ese is NULL:
        return ERROR "ESE marks not found or not approved for this entry."

    # Step 3: Fetch course definition for max marks
    course = query courses WHERE course_code = course_code

    # Step 4: Compute weighted total (out of 100)
    ia_percentage  = (ia.total_ia / course.max_ia_marks) * 40
    ese_percentage = (ese.ese_marks_obtained / course.max_ese_marks) * 60

    if ese.is_absent = TRUE:
        ese_percentage = 0

    total_marks = ia_percentage + ese_percentage

    # Step 5: Determine letter grade and grade point from grading scale
    grade_row = query grading_scale
                WHERE min_percentage <= total_marks
                  AND max_percentage >= total_marks

    letter_grade = grade_row.letter_grade
    grade_point  = grade_row.grade_point
    is_pass      = grade_row.is_pass
    is_backlog   = NOT is_pass

    # Step 6: Upsert result record
    UPSERT INTO results (student_id, course_code, semester, academic_year,
                         total_marks, letter_grade, grade_point, is_pass, is_backlog)
           VALUES (student_id, course_code, semester, academic_year,
                   total_marks, letter_grade, grade_point, is_pass, is_backlog)

    # Step 7: Log the computation event
    INSERT INTO audit_log (action, entity_type, entity_id, new_value)
           VALUES ('GRADE_COMPUTED', 'result', student_id + '_' + course_code,
                   total_marks + ' → ' + letter_grade)

    return SUCCESS { total_marks, letter_grade, grade_point, is_pass }
```

---

#### Component 2: `compute_sgpa(student_id, semester, academic_year)`

```
function compute_sgpa(student_id, semester, academic_year):

    # Step 1: Fetch all results for this student-semester
    results_list = query results
                   WHERE student_id   = student_id
                     AND semester     = semester
                     AND academic_year = academic_year

    if results_list is EMPTY:
        return ERROR "No result records found for this semester."

    # Step 2: For each course, get credit hours
    total_weight = 0
    total_credits = 0

    FOR EACH result IN results_list:
        course = query courses WHERE course_code = result.course_code
        total_weight  += result.grade_point * course.credit_hours
        total_credits += course.credit_hours

    if total_credits = 0:
        return ERROR "Total credit hours are zero; cannot compute SGPA."

    # Step 3: Compute SGPA
    sgpa = total_weight / total_credits
    sgpa = ROUND(sgpa, 2)

    # Step 4: Update SGPA in all result records for this semester
    UPDATE results SET sgpa = sgpa
    WHERE student_id = student_id
      AND semester   = semester
      AND academic_year = academic_year

    return SUCCESS { sgpa }
```

---

#### Component 3: `submit_ia_marks(faculty_id, course_code, semester, academic_year)`

```
function submit_ia_marks(faculty_id, course_code, semester, academic_year):

    # Step 1: Verify faculty assignment
    course = query courses WHERE course_code = course_code AND faculty_id = faculty_id
    if course is NULL:
        return ERROR "Faculty is not assigned to this course."

    # Step 2: Check if mark-entry window is open
    window = query academic_settings
             WHERE key = 'ia_entry_open'
               AND semester = semester
    if window.value ≠ 'TRUE':
        return ERROR "Internal assessment mark entry period is closed."

    # Step 3: Fetch all draft IA marks for this course-semester
    marks = query ia_marks
            WHERE course_code   = course_code
              AND semester      = semester
              AND academic_year  = academic_year
              AND entered_by    = faculty_id
              AND status        = 'Draft'

    if marks is EMPTY:
        return ERROR "No draft marks found to submit."

    # Step 4: Validate completeness — all enrolled students must have marks
    enrolled_students = query student_course_enrolments
                        WHERE course_code = course_code AND semester = semester

    FOR EACH student IN enrolled_students:
        if student.student_id NOT IN marks:
            return ERROR "Marks missing for student: " + student.full_name

    # Step 5: Update status to 'Submitted'
    UPDATE ia_marks SET status = 'Submitted', submitted_at = NOW()
    WHERE course_code   = course_code
      AND semester      = semester
      AND academic_year  = academic_year
      AND entered_by    = faculty_id

    # Step 6: Notify HOD
    hod = query faculty WHERE is_hod = TRUE AND department = course.department
    INSERT INTO notifications (recipient_user_id, notif_type, message)
           VALUES (hod.user_id, 'approval_request',
                   'IA marks submitted by ' + faculty.name +
                   ' for ' + course.course_name + ' — Semester ' + semester +
                   '. Awaiting your approval.')

    # Step 7: Log action
    INSERT INTO audit_log (user_id, action, entity_type, entity_id)
           VALUES (faculty_id, 'IA_MARKS_SUBMITTED', 'ia_marks',
                   course_code + '_' + semester + '_' + academic_year)

    return SUCCESS "Marks submitted for HOD approval. Notification sent."
```

---

#### Component 4: `generate_marksheet_pdf(student_id, semester, academic_year)`

```
function generate_marksheet_pdf(student_id, semester, academic_year):

    # Step 1: Verify that results are published
    first_result = query results
                   WHERE student_id   = student_id
                     AND semester     = semester
                     AND academic_year = academic_year
                     AND published    = TRUE
                   LIMIT 1

    if first_result is NULL:
        return ERROR "Results for this semester are not yet published."

    # Step 2: Fetch student details
    student = query students WHERE student_id = student_id

    # Step 3: Fetch all results for the semester
    results_list = query results
                   JOIN courses USING (course_code)
                   WHERE results.student_id   = student_id
                     AND results.semester     = semester
                     AND results.academic_year = academic_year

    # Step 4: Fetch SGPA (from results) and CGPA
    sgpa = results_list[0].sgpa
    cgpa = compute_cgpa(student_id)                  -- separate function

    # Step 5: Generate a unique document reference number
    doc_ref = 'SRMS/' + academic_year + '/SEM' + semester + '/' + student_id

    # Step 6: Build PDF document
    pdf = create_pdf_document()
    pdf.add_header(university_logo, university_name, 'B.Voc Software Development - Mark Sheet')
    pdf.add_student_info(student.full_name, student.student_id,
                         student.batch_year, student.photo_url)
    pdf.add_results_table(results_list)              -- Course | Max | Obtained | Grade | GP
    pdf.add_footer(sgpa, cgpa, doc_ref, hod_signature, registrar_signature)

    # Step 7: Save and return PDF
    file_path = '/generated_documents/' + doc_ref.replace('/','_') + '.pdf'
    pdf.save(file_path)

    # Step 8: Log download event
    INSERT INTO audit_log (action, entity_type, entity_id)
           VALUES ('MARKSHEET_DOWNLOADED', 'result', doc_ref)

    return SUCCESS { file_path }
```

---

## 9. Benefits of the Proposed System

The implementation of the SRMS will deliver the following quantifiable and qualitative benefits to the university and all stakeholders:

### 9.1 For Students

| Benefit | Detail |
|---|---|
| **24/7 Instant Result Access** | Students can view results immediately upon publication, from any device, without visiting campus. |
| **Accurate, Consistent Grading** | Automated grade computation eliminates manual arithmetic errors and ensures equitable grading across all students. |
| **On-Demand Official Documents** | Mark sheets and transcripts can be downloaded in minutes rather than waiting weeks for manual printing. |
| **Backlog Clarity** | Students receive clear, real-time visibility of pending arrear courses and their impact on CGPA. |
| **Timely Notifications** | Email and SMS alerts ensure students are immediately informed when results are published. |

### 9.2 For Faculty

| Benefit | Detail |
|---|---|
| **Reduced Administrative Burden** | Simple online mark-entry forms replace tedious paper lists and manual submission. |
| **Real-Time Validation** | In-form validation catches errors at entry time, preventing embarrassing mark corrections post-submission. |
| **Transparent Process** | Faculty can track the approval status of their submitted marks in real time. |
| **Better Teaching Insights** | Course-level analytics help faculty identify students who need targeted support. |

### 9.3 For Administration (HOD, Exam Cell, Registrar)

| Benefit | Detail |
|---|---|
| **Faster Result Processing** | Multi-step approval workflow reduces result publication from 21 days to ≤ 5 working days. |
| **Audit Trail & Accountability** | Every action is logged with user, timestamp, and justification — essential for regulatory compliance. |
| **Elimination of Data Silos** | Single, centralised database replaces fragmented Excel files and paper registers. |
| **One-Click Report Generation** | Consolidated class mark sheets, analytics reports, and trend analyses available instantly. |
| **Historical Data Access** | Decade-long academic records accessible in seconds via search. |

### 9.4 For the Institution

| Benefit | Detail |
|---|---|
| **Enhanced Institutional Credibility** | A digital, professional result management system improves the university's reputation, especially for a technology programme. |
| **Regulatory Compliance** | Tamper-evident audit logs and secure data retention support compliance with UGC and government education regulations. |
| **Foundation for Future Expansion** | The modular architecture allows the system to be extended to other programmes and departments in subsequent phases. |
| **Cost Reduction** | Reduced paper, printing, and administrative overtime costs over time. |

---

## 10. Constraints and Assumptions

### 10.1 Constraints

| ID | Constraint | Description |
|---|---|---|
| **CON-01** | **Budget** | The project budget is fixed at the amount agreed in the procurement contract. No scope or technology changes shall be permitted that exceed this budget without formal change-order approval. |
| **CON-02** | **Academic Calendar Deadline** | The system must be fully operational before the commencement of the end-semester examination period for the Academic Year 2025–26. |
| **CON-03** | **Technology Environment** | The system must be deployable on the university's existing Linux-based server infrastructure, without requiring new hardware procurement beyond what is specified in the technical proposal. |
| **CON-04** | **Grading Policy** | The system's grade computation logic must strictly conform to the university's official grading ordinance, as issued by the Academic Council. Any changes to this policy after sign-off are out of scope. |
| **CON-05** | **Data Migration** | The system will not automatically migrate historical semester data from existing Excel files; the university will provide migrated data in the agreed CSV template format. |
| **CON-06** | **Single Programme Scope** | This version (v1.0) covers only the B.Voc Software Development Programme. Extension to other programmes is a future enhancement. |
| **CON-07** | **Internet Connectivity** | The system assumes reliable internet connectivity at the university premises. It is not designed to function offline. |

### 10.2 Assumptions

| ID | Assumption | Description |
|---|---|---|
| **ASM-01** | Each student is uniquely identified by a university-assigned Student ID that remains constant throughout the programme. |
| **ASM-02** | Each course in the B.Voc programme is taught by exactly one primary faculty member per semester cohort. |
| **ASM-03** | The university's official grading scale and academic regulations are provided in written form to the development team in Phase 0 and do not change during the development period. |
| **ASM-04** | The Examination Cell will provide ESE marks in the agreed CSV template format within 5 working days of the examination conclusion. |
| **ASM-05** | The university's IT Department will provide and maintain the server infrastructure, SSL certificate, domain access, and SMTP credentials required for deployment. |
| **ASM-06** | All end users (students, faculty, admin staff) possess basic digital literacy and can use a web browser on a computer or smartphone. |
| **ASM-07** | The system will be used exclusively within the territory governed by Indian data protection regulations. |
| **ASM-08** | A UAT period of at least two working weeks will be available before final go-live. |

---

## 11. Possible Risks

> *This section expands upon the Risk Table presented in Section 7.4 with additional context and contingency planning.*

### 11.1 Technical Risks

| Risk | Likelihood | Impact | Contingency |
|---|---|---|---|
| **Grade computation logic flaw** — an error in the computation engine produces incorrect grades for all students simultaneously | Low | Critical | Independent code review by a senior developer before deployment; automated test suite with 100+ known-correct test cases. |
| **Database corruption during result publication** — a concurrent write conflict corrupts result records | Very Low | Critical | Transaction-based writes with rollback support; daily automated backups with point-in-time recovery capability. |
| **PDF generation failure during peak demand** — the document engine crashes under concurrent download requests | Low | High | Implement PDF generation as an asynchronous queue; pre-generate documents during off-peak hours after publication. |
| **Integration failure with SMS/Email gateway** — notification service is unavailable during result publication | Medium | Medium | Implement retry logic with exponential back-off; fallback to in-portal notification if external gateway fails. |

### 11.2 Operational Risks

| Risk | Likelihood | Impact | Contingency |
|---|---|---|---|
| **Faculty delays in IA mark submission** — faculty do not submit marks on time, blocking the approval workflow | High | Medium | Implement automated reminder notifications 3 days before submission deadline; HOD dashboard shows outstanding submissions in red. |
| **Examinations cell uploads incorrect ESE data** — a wrong Excel file is uploaded | Medium | High | Two-stage validation: format check on upload, followed by a preview-and-confirm screen before data is committed. |
| **Mass simultaneous student logins** crashing the server immediately after result publication | Medium | High | Stagger notifications by 5-minute intervals per batch; use server auto-scaling if cloud-hosted. |

### 11.3 Human & Organisational Risks

| Risk | Likelihood | Impact | Contingency |
|---|---|---|---|
| **Resistance to change** — senior faculty or administration reluctant to abandon the existing Excel-based process | Medium | High | Involve key stakeholders in UAT from Phase 0; demonstrate the system's ease-of-use through live demonstrations. |
| **Contractual disputes** — university requests significant feature additions post-contract | Medium | Medium | Maintain a formal change-request register; all additions to be separately scoped, costed, and approved. |
| **Staff turnover** at the university — system super-administrator leaves before knowledge transfer is complete | Low | High | Provide comprehensive system administration manual; conduct training for at least two university IT staff members. |

---

## 12. Conclusion and Recommendations

### 12.1 Conclusion

The B.Voc Software Development Programme's current student result management process is fundamentally inadequate. The reliance on paper registers, manually compiled spreadsheets, and informal communication channels is not merely inconvenient — it is a structural liability. It exposes the university to risks of data loss, grade disputes, compliance failures, and reputational damage, particularly severe for a programme dedicated to teaching software development.

This Problem Statement and System Analysis Report has presented a comprehensive, evidence-based case for the development of the **Student Result Management System (SRMS)** — a purpose-built, role-based, web-accessible platform designed to modernise every facet of academic result management for the programme.

The analysis within this document has:

- Identified and articulated **twelve specific operational problems** with the current system
- Defined a **complete stakeholder map** with ten distinct user groups
- Specified **48 functional requirements** across eleven modules
- Enumerated **20 non-functional requirements** covering performance, security, reliability, usability, and compliance
- Demonstrated the system's scope, boundaries, and integration points through **DFD diagrams and data dictionary tables**
- Provided **four detailed use case descriptions** for critical system workflows
- Quantified the project as **194 Unadjusted Function Points** with an estimated effort of **582 person-hours** and a delivery timeline of **10–12 weeks**
- Catalogued **13 risk items** with mitigation and contingency strategies
- Presented a complete **three-tier architectural blueprint** with a full PostgreSQL database schema
- Delivered **pseudocode for four key system components**

The SRMS, as specified, is technically feasible, financially justified, and strategically essential for the university.

---

### 12.2 Recommendations

The following recommendations are made to both the university client and the contracted software development company:

| Priority | Recommendation |
|---|---|
| **P1 — Critical** | **Convene a requirements sign-off meeting** between the university academic committee, Examination Cell, and the development company before Phase 1 begins. Freeze requirements formally before design commences. |
| **P1 — Critical** | **Obtain the official grading ordinance document** from the Academic Office in written form. The Grade Computation Engine must be independently verified against at least 50 manually calculated test cases before UAT. |
| **P1 — Critical** | **Plan and conduct data migration** well before the go-live date. The university must clean, validate, and convert existing student records into the agreed CSV format. Allow at least two weeks for this activity. |
| **P2 — High** | **Engage actual end-users early** (at least one faculty member, one HOD representative, and one student representative) in the UI design review during Phase 1. This will improve adoption and reduce change requests post-launch. |
| **P2 — High** | **Implement a parallel-run period** — run the new system alongside the existing Excel-based process for the first semester of deployment. Compare outputs to validate the system before fully decommissioning the manual process. |
| **P2 — High** | **Conduct a security penetration test** before go-live, covering authentication bypass attempts, privilege escalation, and SQL injection vectors. |
| **P3 — Medium** | **Plan for mobile responsiveness from day one** — a significant proportion of students will access results via smartphones. Ensure UI testing includes real mobile devices. |
| **P3 — Medium** | **Design the grading scale as fully configurable** from the administrative panel, not hard-coded, so future changes by the Academic Council can be accommodated without code deployments. |
| **P3 — Medium** | **Document and plan for future phases** — specifically, the extension of SRMS to other departments and programmes. The modular architecture recommended herein supports this direction. |
| **P4 — Low** | **Consider adding a parent/guardian portal** (view-only) in Phase 2, allowing parents to receive automated result notifications. This is explicitly out of scope for v1.0 but should be designed for in the data model. |

---

### 12.3 Next Steps

Upon acceptance of this Problem Statement and System Analysis Report by both parties:

1. **Week 1:** Formal project kick-off meeting; contract signing; team onboarding.
2. **Weeks 1–2:** Requirements sign-off; grading scale documentation received; student and Faculty data format agreed.
3. **Week 2 onwards:** Phase 1 (System Design) commences per the project schedule in Section 7.3.
4. **Ongoing:** Weekly status reporting by the development company to the university project coordinator.

---

*This document has been prepared in accordance with standard software engineering requirements documentation practices. It is intended to serve as the authoritative reference for all subsequent design, development, testing, and deployment activities related to the Student Result Management System for the B.Voc Software Development Programme.*

---

**Document Control**

| Version | Date | Author | Changes |
|---|---|---|---|
| 0.1 | April 20, 2026 | University Academic Systems Committee | Initial draft |
| 0.2 | April 24, 2026 | University Academic Systems Committee | Stakeholder review incorporated |
| 1.0 | April 27, 2026 | University Academic Systems Committee | Final version — submitted to software company |

---

> *© 2026 — University Academic Division. All rights reserved. This document is confidential and intended solely for the use of the contracted software development company and authorised university personnel.*

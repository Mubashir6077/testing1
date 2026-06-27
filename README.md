# MasterLift Equipment Maintenance Notification System


<p align="center">
A Java Swing desktop application for managing industrial equipment, maintenance schedules, document attachments, and automated email notifications.
</p>

---

##  Overview

The **MasterLift Equipment Maintenance Notification System** is a desktop application developed using **Java Swing** and **MySQL** to simplify the management of industrial equipment maintenance.

The application enables administrators to register equipment, assign maintenance frequencies, upload related documents, manage recipients, and automatically send maintenance reminder emails before scheduled service dates.

The system is designed to eliminate manual tracking and ensure that maintenance activities are performed on time.

---

#  Features

##  Equipment Management

* Add new equipment
* Update equipment information
* Delete equipment
* View equipment details
* Search equipment records
* Store manufacturing information
* Track equipment location

---

##  Maintenance Scheduling

Automatically generates maintenance schedules based on the selected maintenance frequency.

Supported frequencies include:

* Annual
* Semi-Annual
* Every Four Months

The system calculates upcoming maintenance dates and stores them in the database.

---

##  Automatic Email Notifications

Integrated with **Jakarta Mail (SMTP)** for automated notifications.

Features include:

* Daily notification scheduler
* Automatic reminder emails
* Multiple recipients
* Equipment-specific recipients
* Manual email testing
* Email delivery tracking

---

##  Recipient Management

Manage maintenance notification recipients.

Features:

* Add recipient
* Remove recipient
* Assign recipients to equipment
* Multiple recipients per equipment

---

##  Document Management

Upload and manage equipment-related documents.

Supports:

* Manuals
* Certificates
* Maintenance Reports
* Inspection Documents
* Images

Operations:

* Upload
* Download
* Delete

---

##  Search & Filter

Quickly search equipment using:

* Stock Number
* Serial Number
* Equipment Type
* Area
* Year

---

##  Database Integration

Uses JDBC for database operations.

Supports:

* Insert
* Update
* Delete
* Search
* Relationships
* File Storage

---

#  Technology Stack

| Technology   | Description           |
| ------------ | --------------------- |
| Java         | Programming Language  |
| Java Swing   | Desktop GUI Framework |
| JDBC         | Database Connectivity |
| MySQL        | Database              |
| Jakarta Mail | Email Notifications   |
| Maven        | Dependency Management |

---

#  Project Structure

```text
src/
│
├── MasterliftwithInterface26.java
├── DatabaseConnection.java
├── EmailScheduler.java
├── EmailSender.java
├── AttachmentManager.java
├── RecipientManager.java
└── Utility Classes
```

---

#  How It Works

```
Equipment Registration
          │
          ▼
Generate Maintenance Schedule
          │
          ▼
Save into Database
          │
          ▼
Daily Scheduler
          │
          ▼
Check Upcoming Maintenance
          │
          ▼
Send Reminder Emails
```

---

#  Database Design

### Equipment

Stores equipment information.

Example fields:

* Equipment ID
* Stock Number
* Serial Number
* Equipment Type
* Manufacturing Year
* Area
* Maintenance Frequency
* First Maintenance Month

---

### Equipment Files

Stores uploaded documents associated with equipment.

Example fields:

* File ID
* Equipment ID
* File Name
* File Data

---

### Scheduled Emails

Stores all automatically generated maintenance notifications.

Example fields:

* Email ID
* Equipment ID
* Notification Date
* Maintenance Date
* Status

---

### Recipients

Stores maintenance recipients.

Example fields:

* Recipient ID
* Name
* Email Address

---

#  Installation

## Prerequisites

* Java JDK 17 or later
* MySQL Server
* Maven
* IDE (IntelliJ IDEA, Eclipse, or NetBeans)

---

## Configure Database

Create a MySQL database and update the database credentials inside the project.

Example:

```java
String url = "jdbc:mysql://localhost:3306/masterlift";
String username = "root";
String password = "password";
```

---

## Run Application

Open the project in your preferred IDE and run:

```
MasterliftwithInterface26.java
```

---

#  Screenshots

> Replace the images below with screenshots from your application.

---

## Dashboard

![Dashboard](docs/screenshots/dashboard.png)

---

## Equipment Management

![Equipment Management](docs/screenshots/equipment-management.png)

---

## Add Equipment

![Add Equipment](docs/screenshots/add-equipment.png)

---

## Equipment Details

![Equipment Details](docs/screenshots/equipment-details.png)

---

## Maintenance Schedule

![Maintenance Schedule](docs/screenshots/maintenance-schedule.png)

---

## Recipient Management

![Recipient Management](docs/screenshots/recipient-management.png)

---

## Email Notification

![Email Notification](docs/screenshots/email-notification.png)

---

## File Attachment

![File Attachment](docs/screenshots/file-attachment.png)

---

## Search Equipment

![Search Equipment](docs/screenshots/search-equipment.png)

---

#  Email Notification Workflow

```
Application Starts
        │
        ▼
Load Scheduled Emails
        │
        ▼
Compare Today's Date
        │
        ▼
Notification Due?
        │
   Yes / No
        │
        ▼
Collect Equipment Information
        │
        ▼
Generate Email
        │
        ▼
Send Email using SMTP
        │
        ▼
Mark Notification as Sent
```

---

#  Suggested Folder Structure

```
MasterLift/
│
├── docs/
│   └── screenshots/
│
├── database/
│   └── masterlift.sql
│
├── src/
│
├── lib/
│
├── pom.xml
│
└── README.md
```

---

#  Future Improvements

* User Authentication
* Role-Based Access Control
* PDF Report Generation
* Dashboard Analytics
* SMS Notifications
* Calendar View
* Export to Excel
* Equipment QR Codes
* Cloud Storage Integration
* REST API Support
* Dark Mode

---


#  License

This project is licensed under the MIT License.

---

#  Author

**Boris**

Computer Science
Java Developer | Software Engineer

---

#  Acknowledgements

* Java Swing
* MySQL
* JDBC
* Jakarta Mail API
* Maven

---


# Hospital Appointment Booking System

## Project Overview

This project is a **Hospital Appointment Booking System** designed to manage patient appointments, doctor details, treatments, specializations, and room assignments within a hospital or clinic. The system is built using **MySQL** as the database management system, with relational tables structured to handle patient and doctor information, room assignments, appointment scheduling, treatments, and specializations.

### Key Features:
- **Patient Management**: Store patient details including name, email, contact info, and gender.
- **Doctor Management**: Store doctor details and their associated specializations.
- **Appointment Scheduling**: Schedule, update, and manage appointments, with room assignments and doctor assignments.
- **Treatment Management**: Assign treatments to appointments with cost details.
- **Specialization Management**: Track different medical specializations and link them to doctors.

## Database Schema

The database schema is designed using relational tables with various relationships such as one-to-one (1:1), one-to-many (1:M), and many-to-many (M:M). The tables and relationships are structured to ensure proper management of hospital appointments, patients, doctors, treatments, and specializations.

Below is the **ER Diagram** for the database:

## ER Diagram

![ER Diagram](https://www.plantuml.com/plantuml/dpng/hPJ1ZjGm38RlUOfeBu3GlC2U5ea7GC0zSXFFD58ILuaBB0plJjDcD7Mdg4BYjCflr_xywzzvAGoPnnZK6_q9s6DYpT05L9ZOywj-QkgJ_gMqVZyiB-ETVjO-STNEOmWcGSH9-WRPzf2hZ15yaDBGKzfqEM0qT3QTpznFfVgk-WMJmxpg_Qqcn8zacVA6S14Re9iV_u-lznbDXMfi2yUN0Qs7u7y2UqeR7bbiN4M8WkyHpM6nsG-rSoem_k2zjMRjXduR8RsUc4xrhyuO5hGE-JjYkZa7oMsclFiBjpcoTV-YHlgPA6vigLARbecYc3KBQOmTPkd4EH3bzU0Fmq3J8pu6TLLfQw0fCh3x8TuUA3zV9u1znFb-1XwBm1M7DU2l6M4Fj-fhMBwz_paRLRLKkFAXzH72WrL6KXobHRWCoTsFkATbE_tOU76ZJ4lRNte_57Nx7RfUJoUw2fPdtKDHBSkxTKl9ZPQBgd7RRu5I_2MXCqnAPhxrx_-VoUK7dHq6IfTILwoNInxftMo83QF3effu_CNiQ54lE5qTmny0)

## Database Structure

The following tables are created to manage the hospital's data:

1. **Patient Table**
   - Stores information about patients such as their name, email, contact details, date of birth, and gender.

2. **Doctor Table**
   - Stores details about doctors including their name, email, phone, and hire date.

3. **Specialization Table**
   - Defines different specializations that doctors can belong to (e.g., Cardiology, Neurology, etc.).

4. **Specialization_Doctor Table**
   - Many-to-many relationship between doctors and their specializations.

5. **Room Table**
   - Rooms where appointments are scheduled.

6. **Appointment Table**
   - Manages the relationship between patients, doctors, and the rooms they occupy during appointments.

7. **Treatment Table**
   - Lists treatments that may be assigned to appointments.

8. **Appointment_Treatment Table**
   - Many-to-many relationship between appointments and treatments.

## Installation

To set up the project and use the database, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/hospital-appointment-booking-system.git

Import the SQL File:

Navigate to your MySQL database client (e.g., MySQL Workbench, phpMyAdmin, or command line).

Run the provided hospital_appointment.sql script to create the necessary tables and relationships in the database.

sql

SOURCE /path/to/hospital_appointment.sql;
Set Up Your Database:

After running the SQL script, the database will be ready to use. You can begin interacting with it by inserting records, querying data, and testing the appointment scheduling system.

Usage
Once the database is set up, you can perform CRUD (Create, Read, Update, Delete) operations on the tables.

Use the Patient, Doctor, Appointment, Treatment, and Specialization tables to manage hospital data.

The relationships between tables allow you to link patients to doctors, doctors to specializations, and appointments to treatments.

Example SQL Queries:
Insert a New Patient:

sql

INSERT INTO Patient (full_name, email, phone, date_of_birth, gender) 
VALUES ('John Doe', 'patiente@example.com', '1234567890', '1990-01-01', 'Male');
Create a New Appointment:

sql

INSERT INTO Appointment (patient_id, doctor_id, appointment_date, room_id) 
VALUES (1, 2, '2025-05-15 10:00:00', 1);
Contributions
Contributions to this project are welcome! Please feel free to fork the repository, create issues, or submit pull requests with improvements.

To contribute:
Fork the repository.

Create a new branch (git checkout -b feature-branch).

Make your changes and commit them (git commit -am 'Add new feature').

Push to your branch (git push origin feature-branch).

Create a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.
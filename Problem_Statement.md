
# Title

Medical Lab Test Booking & Report Portal

# Domain

Healthcare Management System

# Who is the User?

1. Patient
Register and log in.
View available lab tests.
Book laboratory tests.
View booking history.
Download test reports.

2. Laboratory Staff
Log in securely.
View patient bookings.
Update booking status.
Upload laboratory test reports.

3. Administrator
Manage users.
Manage laboratory tests.
Monitor bookings.
Manage reports.
View system statistics.

# What Problem Are We Solving? 

Many diagnostic laboratories still rely on manual appointment booking and paper-based report distribution, which leads to long waiting times, misplaced records, and inefficient management. Patients often need to visit the laboratory multiple times to schedule tests and collect reports. Laboratory staff also spend considerable time maintaining records manually. This project provides a secure web portal where patients can book laboratory tests online, while laboratory staff upload reports digitally, allowing patients to access them anytime.

# Proposed Solution

The proposed Medical Lab Test Booking & Report Portal provides:

Patient Registration and Login
Laboratory Staff and Admin Login
View Available Lab Tests
Online Lab Test Booking
Booking History
Report Upload by Laboratory Staff
Report Download by Patients
Laboratory Test Management
User Management
Dashboard for Admin and Staff

# Core Entities / Database Tables

Users
user_id
name
email
phone
password
role
Lab_Tests

test_id
test_name
description
price
Bookings
booking_id
user_id
test_id
booking_date
status
Reports
report_id
booking_id
report_file
remarks
upload_date
Feedback
feedback_id
user_id
booking_id
rating
comments
Relationships
One User → Many Bookings
One Booking → One Lab Test
One Booking → One Report
One User → Many Feedback entries

This satisfies the requirement of five database tables with real relationships.

# User Roles & Permissions

Patient
Register
Login
View available tests
Book lab tests
View booking history
Download reports
Submit feedback
Laboratory Staff
Login
View bookings
Update booking status
Upload reports
Administrator
Login
Manage users
Manage laboratory tests
View all bookings
Monitor reports
View feedback

# Success Criteria

The project will be considered successful if:

A patient can register successfully.
A patient can log in securely.
A patient can book a laboratory test in less than one minute.
Laboratory staff can upload reports successfully.
Patients can download uploaded reports.
Administrators can manage users and laboratory tests.
All data is stored correctly in the MySQL database.
Different users can access only their authorized features.

# Out of Scope

The following features are intentionally excluded from this version:

Online Payment Gateway
SMS Notifications
Email Verification
OTP Login
AI Disease Prediction
Chatbot
Video Consultation
Mobile Application
QR Code Report Verification
Voice Assistant

These can be added in future versions.

# Chosen Track

python (FastAPI)
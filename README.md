**Project overview**
This project is an Airbnb clone that aims to replicate the core functionalities of the Airbnb platform, allowing users to search for, book, and manage listings for short-term rentals. The goal is to provide a user-friendly experience for both guests and hosts, featuring a responsive design and robust backend functionality.

**Project Goals**
User Authentication: Enable secure sign-up and login for users.
Property Listings: Allow hosts to create and manage property listings with detailed descriptions, images, and pricing.
Search and Filter: Implement search functionality for users to find listings based on location, price, and amenities.
Booking System: Facilitate booking processes, including date selection and payment integration.
User Reviews: Enable users to leave reviews and ratings for properties.

**Tech Stack**
Django
MySQL

**Team Roles**
1. Backend Developer
Responsibilities: Develops server-side logic, APIs, and ensures application security.
2. Frontend Developer
Responsibilities: Builds user interface, integrates APIs, and optimizes performance.
3. Database Administrator (DBA)
Responsibilities: Manages database design, integrity, and optimization.
4. DevOps Engineer
Responsibilities: Sets up CI/CD pipelines, monitors infrastructure, and manages deployments.
5. Quality Assurance (QA) Engineer
Responsibilities: Tests the application for functionality, reports bugs, and ensures quality.
6. Product Manager
Responsibilities: Defines project scope, coordinates teams, and aligns development with business goals.
7. UI/UX Designer
Responsibilities: Designs user interfaces, conducts research, and ensures a great user experience.

**Technology Stack**
Django: A web framework for building RESTful APIs and managing backend logic efficiently.
MySQL: A robust relational database management system for storing and retrieving user data and property listings.
RESTful APIs: Architectural style for designing networked applications, allowing communication between the frontend and backend.

**Database Design**
**User**
***Important Fields***
user_id: Unique identifier for the user.
name: Full name of the user.
email: Email address for user authentication.
password: Hashed password for security.
role: Indicates if the user is a guest or a host.

**Property**
***Important Fields***
property_id: Unique identifier for the property.
title: Title of the property listing.
description: Detailed description of the property.
price_per_night: Cost per night for booking.
host_id: Foreign key linking to the user who owns the property.

**Booking**
***Important Fields***
booking_id: Unique identifier for the booking.
property_id: Foreign key linking to the property being booked.
user_id: Foreign key linking to the user who made the booking.
start_date: Check-in date for the booking.
end_date: Check-out date for the booking.

**Review**
***Important Fields***
review_id: Unique identifier for the review.
property_id: Foreign key linking to the reviewed property.
user_id: Foreign key linking to the user who wrote the review.
rating: Numerical rating given by the user.
comment: Text feedback about the property.

**Payment**
***Important Fields***
payment_id: Unique identifier for the payment.
booking_id: Foreign key linking to the associated booking.
amount: Total amount paid.
payment_date: Date of the payment transaction.
status: Status of the payment (e.g., completed, pending).

**Entity Relationships**
User ↔ Property: A user can own multiple properties (one-to-many).
User ↔ Booking: A user can have multiple bookings (one-to-many).
Property ↔ Booking: A booking belongs to one property, but a property can have multiple bookings (one-to-many).
User ↔ Review: A user can write multiple reviews (one-to-many).
Property ↔ Review: A property can have multiple reviews (one-to-many).
Booking ↔ Payment: A payment is associated with one booking (one-to-one).
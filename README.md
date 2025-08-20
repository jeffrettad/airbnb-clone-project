## Overview of the AirBnB Clone
# 🚀  Objective
The backend for the Airbnb Clone project is designed to provide a robust and scalable foundation for managing user interactions, property listings, bookings, and payments. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.

# 🏆  Project Goals
User Management: Implement a secure system for user registration, authentication, and profile management.
Property Management: Develop features for property listing creation, updates, and retrieval.
Booking System: Create a booking mechanism for users to reserve properties and manage booking details.
Payment Processing: Integrate a payment system to handle transactions and record payment details.
Review System: Allow users to leave reviews and ratings for properties.
Data Optimization: Ensure efficient data retrieval and storage through database optimizations.

# ⚙️  Technology Stack
- Django: A high-level Python web framework used for building the RESTful API.
- Django REST Framework: Provides tools for creating and managing RESTful APIs.
- PostgreSQL: A powerful relational database used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.

## Team Roles
+ Backend Developer: back-end developer are not only write code but also do the tasks of an architect—for example, devise an app architecture or design and implement the necessary integrations
+ Database Administrator & DevOps Engineer: They oversee and facilitate code releases on a CI/CD basis.
+ QA Engineer:
  
(i) They makes sure an application performs according to requirements

(ii) They Spots functional and non-functional defects

# Database Design
# User

- id, name, email, role

- A user can own multiple Properties

- A user can make multiple Bookings

- A user can leave multiple Reviews

- A user can make multiple Payments

# Property

- id, title, description, location, price_per_night

- Belongs to a User (host)

- Has many Bookings

- Has many Reviews

# Booking

- id, user_id, property_id, start_date, end_date, status

- Belongs to a User (guest)

- Belongs to a Property

- Has many Payments

# Review

- id, user_id, property_id, rating, comment

- Belongs to a User

- Belongs to a Property

# Payment

- id, booking_id, amount, payment_method, status

  - Belongs to a Booking

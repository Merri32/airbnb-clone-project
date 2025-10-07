# Airbnb Clone Project

## Overview
The goal of this project is to build an Airbnb clone web application where users can list, browse, and book stays.

## Tech Stack
- HTML, CSS, JavaScript (Frontend)
- Python (Backend)
- Flask or Django Framework
- Git & GitHub for version control
 

## Team Roles

- **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.

- **Database Administrator**: Manages database design, indexing, and optimizations.

- **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.

- **QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.


## Technology Stack

- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: Handles asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: A containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automates testing and deployment of code changes for efficient development.


## Database Design

### Key Entities

1. **Users**
   - Fields: `id`, `name`, `email`, `password`, `role`
   - Description: Represents users of the system — both hosts and guests.

2. **Properties**
   - Fields: `id`, `title`, `description`, `price_per_night`, `host_id`
   - Description: Contains details about listed properties. Each property belongs to one host (user).

3. **Bookings**
   - Fields: `id`, `user_id`, `property_id`, `check_in_date`, `check_out_date`
   - Description: Stores booking information. Each booking is linked to one user and one property.

4. **Reviews**
   - Fields: `id`, `user_id`, `property_id`, `rating`, `comment`
   - Description: Users can leave reviews for properties they have stayed in.

5. **Payments**
   - Fields: `id`, `booking_id`, `amount`, `payment_method`, `status`
   - Description: Tracks payment transactions for bookings.

### Entity Relationships
- A **User** can own multiple **Properties**.
- A **Property** can have multiple **Bookings**.
- A **Booking** belongs to one **User** and one **Property**.
- A **Property** can have multiple **Reviews**.
- Each **Booking** has one **Payment**.






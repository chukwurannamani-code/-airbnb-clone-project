# -airbnb-clone-project
This is an application that mimics the airbnb backend system
It will have the following functionalities

## Team Roles
Backend Developer: Backend developers implement the core of an app 
— its algorithms and business logic.
Experienced back-end developers not only write code but also do the
tasks of an architect—for example, devise an app architecture or design and
implement the necessary integrations.

Database Administrator: The Database admin is the one in charge of the database eg postgresql. He ensures that the
database is running efficiently and maintains access to the database
DevOps Engineer: This person is in charge of CI/CD and facilitates cooperation between operations and development teams
QA Engineer: This person is responsible for testing the application to ensure that there are no bugs

## Technology Stack Overview
- GRAPHQL this is the query language in which we will use to interact with our database
-  Django Provides a comprehensive RESTful API for handling CRUD operations on user and property data.
-  Django Rest Framework PProvides tools for creating and managing RESTful APIs.
-  PostgreSQL relational database.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.

## Database Design

### Key entities include
- Users
- Properties
- Bookings
- Reviews
- Payments

Users: name, id, email, phone number 
A user can have multiple bookings, properties, reviews and payments

Properties: Property type, location(longitude, latitude), price, amenities, payment duration
A property will have a user as the owner as well as reviews, payments, bookings attached to that property

Booking: Booking Id, amount, userId
bookings will be done by users and will also have the amount

Reviews: ReviewId, review(int), propertyId, userId
Each review will have a userId, the property that is being reviewed

Payment: PaymentId, propertyId, BookingId
each payment should be for a particular booking, for a particular property

## Feature Breakdown
-  API Documentation: OpenApi standard documentation
-  User Authentication: Register new users, authenticate, and manage user profiles.
-  Property Management: Create, update, retrieve, and delete property listings.
-  Booking System: Make, update, and manage bookings, including check-in and check-out details.
- Payment Processing: Handle payment transactions related to bookings.
- Review System: Post and manage reviews for properties.
- Database Optimizations:  Implement indexes for fast retrieval of frequently accessed data and
  use caching strategies to reduce database load and improve performance.
## Api Security Overview

Security measures include
- Authentication: making sure that only registered users gain access to the apis
- Authorization: Role based authorization to prevent unauthorized people from doing certain tasks.
- Rate limiting: Controlling how many requests a user can make for a period of time to prevent hackers from trying to login to any account
- Security is very important because, users information has to be secure whether it's for payment or for CRUD operations

## CI/CD Pipeline
CICD pipelines are automated workflows that build, test, and deploy
software changes efficiently and reliably, using the principles of continuous integration (CI) and continuous delivery/deployment (CD)
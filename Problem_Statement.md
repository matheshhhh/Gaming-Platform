# Problem Statement

## 1. Title

**Gaming Event Ticketing & Registration Platform**

---

## 2. Domain

**Gaming Event Management**

---

## 3. Who is the user?

The system will have two main types of users:

### 1. User / Student

A user can:

* Create an account and log in.
* View available gaming events.
* View event details such as game name, date, venue, and available slots.
* Create a team and add team members.
* Register a team for a gaming event.
* Book a ticket for an event.
* View their event registrations and booked tickets.

### 2. Admin

An admin can:

* Log in to the system.
* Create new gaming events.
* Update or remove existing events.
* View registered teams and participants.
* View ticket bookings and event registration details.

---

## 4. What problem are we solving?

Gaming events conducted in colleges and small organizations are often managed using different methods such as forms, spreadsheets, and manual registration. This can make it difficult to maintain participant information, manage team registrations, and track available tickets.

The proposed system provides a simple web-based platform where users can view gaming events, create teams, register for events, and book tickets from one place.

For example, if a college conducts a gaming event for games such as Valorant, BGMI, or FIFA, students can use the platform to view the event, create their team, register for the event, and check their registration details. The admin can manage the event and view the registered participants.

---

## 5. Proposed Solution

The proposed application will be a full-stack web application consisting of a React frontend and a Python FastAPI backend.

The application will provide the following features:

* User registration and login.
* JWT-based user authentication.
* Display a list of available gaming events.
* Display detailed information about each event.
* Admin can create, update, and delete gaming events.
* Users can create gaming teams.
* Users can add team members.
* Teams can register for available gaming events.
* Users can book tickets for events.
* Users can view their registrations and tickets.
* Admin can view event registrations and ticket bookings.
* Basic dashboard for users and administrators.

The backend will provide REST APIs for communication between the frontend and database.

---

## 6. Core Entities / Database Tables

The application will use the following main database tables:

### 1. User

Stores user account information such as name, email, password, and role.

### 2. Event

Stores gaming event information such as event name, game, date, venue, description, maximum participants, and available slots.

### 3. Team

Stores information about teams created by users.

### 4. TeamMember

Stores the relationship between users and teams and identifies the members of each team.

### 5. Registration

Stores team registration information for a particular gaming event.

### 6. Ticket

Stores information about tickets booked by users for gaming events.

### Main Relationships

* One user can create multiple teams.
* One team can have multiple team members.
* One event can have multiple team registrations.
* One team can register for multiple events.
* One user can book multiple tickets.
* One event can have multiple ticket bookings.

---

## 7. User Roles & Permissions

| Role  | Permissions                                                                                                                    |
| ----- | ------------------------------------------------------------------------------------------------------------------------------ |
| User  | Register, login, view events, create team, add team members, register for events, book tickets, view registrations and tickets |
| Admin | Login, create events, update events, delete events, view users, view teams, view event registrations, view ticket bookings     |

The system will restrict administrative operations to users with the Admin role.

---

## 8. Success Criteria

The project will be considered successful if:

1. A new user can register and log in successfully.
2. Users can view available gaming events and their details.
3. A user can create a team and add team members.
4. A team can successfully register for an available gaming event.
5. A user can book a ticket for an event.
6. Users can view their event registrations and booked tickets.
7. An admin can create, update, and delete gaming events.
8. An admin can view registered teams and ticket bookings.
9. The application stores and retrieves data correctly from the database.
10. The application can be deployed and accessed through a public URL.

---

## 9. Out of Scope

To keep the project achievable within the capstone duration, the following features are not included in the initial version:

* Real online payment gateway integration.
* Real-time tournament/game integration.
* Live game score tracking.
* Mobile application.
* Live streaming of gaming events.
* Advanced recommendation systems.
* Complex AI-based features in the initial version.
* Physical QR-code scanner integration.
* Multiple microservices.
* Large-scale commercial ticketing functionality.

A small enhancement or AI-related feature may be added later if required for the final phase of the capstone.

---

## 10. Chosen Track

**Python Track**

### Backend

* Python 3.11+
* FastAPI

### Frontend

* React.js
* Axios
* Bootstrap / Tailwind CSS

### Database

* PostgreSQL

### ORM / Data Layer

* SQLAlchemy

### Authentication

* JWT-based authentication
* Password hashing using bcrypt

### Testing

* pytest

### API Documentation

* FastAPI Swagger / OpenAPI

### CI/CD

* GitHub Actions

### Deployment

* Backend: Render
* Frontend: Vercel
* Database: Cloud-hosted PostgreSQL

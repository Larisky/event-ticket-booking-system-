## Overview
The Event Ticket Booking System is a web application designed to facilitate the management of event tickets. It allows users to create events, book tickets for those events, manage cancellations, and maintain a waiting list for users when tickets are sold out. The system is built using Node.js, Express.js, and a MySQL database.

## Purpose
The main goals of this system are to:

Provide a seamless way for event organizers to manage ticket sales.
Allow users to easily book and cancel tickets.
Maintain fairness in ticket allocation through a waiting list mechanism.
Core Functionalities
Event Initialization:

Organizers can create an event and specify the total number of available tickets.
Ticket Booking:

Users can book tickets for events. If all tickets are sold out, the system automatically places them on a waiting list.
Cancellation Handling:

Users can cancel their bookings. If a ticket is canceled, the system checks the waiting list and automatically assigns the ticket to the next user.
Status Retrieval:

Users can check the current status of an event, including the number of available tickets and the size of the waiting list.

## Features

- Initialize events with a specified number of available tickets.
- Book tickets for users, automatically adding them to a waiting list when tickets are sold out.
- Cancel bookings and notify users on the waiting list when tickets become available.
- Retrieve the current status of events, including available tickets and waiting list count.

## Technologies Used

- **Node.js**: JavaScript runtime for building the server.
- **Express.js**: Web framework for creating the RESTful API.
- **Sequelize**: ORM for interacting with the MySQL database.
- **MySQL**: Relational database management system for persistent storage.
- **Jest**: Testing framework for unit and integration tests.
- **Supertest**: Library for testing HTTP endpoints.
- **CORS**: Middleware for enabling cross-origin resource sharing.

set-up......
1. Clone the Repository
2. Install Dependencies
3. Set Up MySQL Database
4. Configure Database Connection
5. Run Migrations
6. Start the Server


API Endpoints

1. Initialize an Event
2. Book a Ticket
3. Cancel a Booking
4. Get Event Status
5. Running test

## Design Choices

### Architecture

- **Microservices Approach**: The system is designed as a set of interconnected services that handle specific functionalities. This separation allows for easier maintenance and scalability in the future.

### Technology Stack

- **Node.js and Express.js**: Chosen for their lightweight and efficient handling of asynchronous operations. This makes the system responsive and capable of handling multiple requests concurrently, which is essential for a ticket booking application.

- **MySQL**: A relational database management system was selected for its robustness and ability to handle complex queries. It provides the necessary data integrity and relationships between events, bookings, and users.

- **Sequelize ORM**: This was used for database interactions to simplify the process of querying and managing the database. It abstracts the SQL syntax and allows for cleaner, more maintainable code.

### API Design

- **RESTful API**: The API endpoints follow REST principles, making them intuitive and easy to use. This design allows for straightforward interaction with the backend using standard HTTP methods (GET, POST).


### Concurrency Handling

- **Race Condition Prevention**: To ensure thread-safety during booking and cancellation processes, a locking mechanism or appropriate error handling is implemented. This prevents situations where multiple users can book the same ticket simultaneously.

### Error Handling

- **Comprehensive Error Management**: The system includes robust error handling to manage various scenarios, such as invalid inputs or database errors. Meaningful error messages are provided to guide users and developers in troubleshooting issues.

### Test-Driven Development (TDD)

- **Unit and Integration Tests**: The system was built with a TDD approach, ensuring that all core functionalities are thoroughly tested before implementation. This practice leads to higher code quality and fewer bugs in production.

### Code Organization

- **Modular Structure**: The codebase is organized into distinct folders (controllers, models, routes, services), promoting modularity and maintainability. Each component has a clear responsibility, making it easier to navigate and update the code in the future.

### Future Scalability

- **Scalable Design**: The choice of technology and architecture allows for future expansion, such as adding new features (like payment processing or user authentication) or scaling to handle more users and events.



Acknowledgments
-Special thanks to Pakam Technology Limited for providing this assessment opportunity.
-Inspired by various ticket booking systems.
-Special thanks to the contributors of the open-source community for their valuable resources and documentation.
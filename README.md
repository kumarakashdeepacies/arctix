
# Project Arctix

**Project Arctix** is a platform designed to bridge the gap between small local businesses offering unique cultural experiences and tourists seeking authentic adventures beyond the typical crowded hotspots. By empowering local vendors to list their services, Arctix provides travelers with the opportunity to discover and book hidden gems, such as guided mountain treks, cultural workshops, and more.

## Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Solution Overview](#solution-overview)
- [Features](#features)
- [User Roles](#user-roles)
  - [Vendor Account](#vendor-account)
  - [Customer Account](#customer-account)
- [High-Level Design](#high-level-design)
  - [System Architecture](#system-architecture)
  - [Component Interaction](#component-interaction)
- [Value Proposition](#value-proposition)
- [Conclusion](#conclusion)

## Introduction

Tourists often miss out on authentic local experiences due to the prominence of popularized destinations. Small businesses and local guides struggle to reach potential customers because they lack visibility on mainstream platforms. Arctix aims to solve this by providing a dedicated platform where these vendors can list their events and services, making them easily discoverable to travelers seeking genuine experiences.

## Problem Statement

- **For Tourists**: Difficulty in discovering authentic, less-commercialized local experiences.
- **For Local Vendors**: Limited visibility and reach to potential customers due to the dominance of popular attractions.

## Solution Overview

Arctix offers a user-friendly platform where:

- **Vendors** can create detailed listings of their events and services, manage bookings, and receive payments.
- **Customers** can discover events around them, read reviews, make bookings, and store tickets digitally.

## Features

- **User Authentication**: Secure login system for both vendors and customers.
- **Two Account Types**: Separate functionalities for vendor and customer accounts.
- **Event Listing**: Vendors can list events with detailed information.
- **Booking System**: Customers can book events directly through the platform.
- **Payment Gateway**: Secure payment processing for event bookings.
- **Location Services**: Customers can find events based on their current location.
- **Reviews and Ratings**: Customers can read and leave reviews for events.
- **Ticket Management**: Digital tickets stored within the customer's account.

## User Roles

### Vendor Account

Vendors can:

- Create and manage event listings.
- Specify event details: price, available seats, location, start and end points, and other relevant information.
- View and manage bookings.
- Receive payments securely.

### Customer Account

Customers can:

- Discover events based on their location.
- View event details, including descriptions, ratings, and reviews.
- Book events and make secure payments.
- Access and manage their digital tickets/passes.

## High-Level Design

### System Architecture

```mermaid
digraph TD
    subgraph Frontend
        A[Customer App] -->|API Calls| C[Web Server]
        B[Vendor App] -->|API Calls| C
    end
    C -->|API Requests| D[Application Server]
    D -->|Database Queries| E[Database]
    D -->|Payment Processing| F[Payment Gateway]
    D -->|Auth Requests| G[Authentication Service]
```

### Component Interaction

- **User Authentication**: Users (vendors/customers) log in via the Authentication Service.
- **Event Management**: Vendors create events through the Vendor App. Event data is stored in the Database.
- **Event Discovery**: Customers use the Customer App to discover events. Location Services fetch events near the user's location.
- **Booking and Payment**: Customers book events via the Application Server. Payments are processed through the Payment Gateway.
- **Ticket Management**: Upon successful payment, tickets are generated and stored in the customer's account.

## Value Proposition

### For Tourists:

- Access to authentic local experiences.
- Easy booking and secure payment.
- Reviews and ratings to make informed decisions.

### For Local Vendors:

- Increased visibility to a wider audience.
- Easy management of events and bookings.
- Secure payment processing.

## Conclusion

Project Arctix aims to enrich the travel experience by connecting tourists with unique local events and experiences, while empowering small businesses and local guides with a platform to reach a broader audience. Through its user-friendly interface and robust features, Arctix bridges the gap between demand and supply in the tourism industry.

# Google Sheets Database Schema for Travel Agency Management System

## Sheets Overview
This document outlines the schema for a Google Sheets database consisting of 14 sheets required for managing a travel agency. Each sheet contains specific columns, their data types, and brief descriptions.

### 1. Customers
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| CustomerID        | Integer     | Unique identifier for each customer          |
| FirstName         | String      | Customer's first name                        |
| LastName          | String      | Customer's last name                         |
| Email             | String      | Customer's email address                     |
| PhoneNumber       | String      | Customer's phone number                      |
| DateOfBirth       | Date        | Customer's date of birth                     |

### 2. Bookings
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| BookingID         | Integer     | Unique identifier for each booking           |
| CustomerID        | Integer     | Reference to the customer making the booking |
| DateOfBooking     | Date        | Date when the booking was made               |
| TotalAmount       | Decimal     | Total amount for the booking                 |
| PaymentStatus      | String      | Status of payment (Paid/Pending)            |

### 3. Destinations
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| DestinationID     | Integer     | Unique identifier for each destination       |
| Name              | String      | Name of the destination                      |
| Country           | String      | Country where the destination is located    |
| Description       | String      | Description of the destination               |
| PopularAttractions | String      | Key attractions located at the destination   |

### 4. Tours
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| TourID            | Integer     | Unique identifier for each tour              |
| DestinationID     | Integer     | Reference to the destination of the tour     |
| Duration           | Integer     | Duration of the tour in days                 |
| Price             | Decimal     | Price per person for the tour                |
| TourGuide         | String      | Name of the tour guide                       |

### 5. Payments
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| PaymentID         | Integer     | Unique identifier for each payment           |
| BookingID         | Integer     | Reference to the booking related to the payment |
| Amount            | Decimal     | Amount paid                                  |
| PaymentDate       | Date        | Date of the payment                          |
| PaymentMethod     | String      | Method of payment (Credit Card/Cash)        |

### 6. Feedback
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| FeedbackID        | Integer     | Unique identifier for each feedback entry    |
| BookingID         | Integer     | Reference to the booking related to the feedback |
| StarRating        | Integer     | Star rating given by the customer (1-5)     |
| Comments          | String      | Customer comments                            |
| FeedbackDate      | Date        | Date when feedback was received              |

### 7. Travel Agents
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| AgentID           | Integer     | Unique identifier for each travel agent      |
| Name              | String      | Name of the travel agent                     |
| Email             | String      | Email address of the travel agent            |
| PhoneNumber       | String      | Phone number of the travel agent             |
| AgencyName        | String      | Name of the agency the agent works for       |

### 8. Employees
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| EmployeeID        | Integer     | Unique identifier for each employee          |
| FirstName         | String      | Employee's first name                        |
| LastName          | String      | Employee's last name                         |
| Position          | String      | Job title of the employee                    |
| Email             | String      | Employee's email                             |

### 9. Packages
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| PackageID         | Integer     | Unique identifier for each package           |
| Name              | String      | Name of the travel package                   |
| Price             | Decimal     | Price of the package                         |
| Description       | String      | Description of the package                   |
| IncludedServices   | String      | List of services included in the package     |

### 10. Locations
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| LocationID        | Integer     | Unique identifier for each location          |
| Name              | String      | Name of the location                         |
| Type              | String      | Type (City/Attraction)                       |
| RelatedDestination| Integer     | Reference to related destination              |
| Description       | String      | Description of the location                  |

### 11. Transport
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| TransportID       | Integer     | Unique identifier for each transport option  |
| Type              | String      | Type of transport (Bus/Train)               |
| Capacity          | Integer     | Maximum capacity of the transport            |
| CostPerMile      | Decimal     | Cost per mile for transport                  |
| Available         | Boolean     | Availability status                          |

### 12. Itineraries
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| ItineraryID       | Integer     | Unique identifier for each itinerary         |
| BookingID         | Integer     | Reference to the booking                     |
| DayNumber         | Integer     | Day of the itinerary                         |
| Activities        | String      | Activities planned for the day              |
| Notes             | String      | Additional notes for the itinerary           |

### 13. Resources
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| ResourceID        | Integer     | Unique identifier for each resource          |
| Type              | String      | Type of resource (Document/Guide)           |
| Path              | String      | Path or URL to access the resource           |
| RelatedTour      | Integer     | Reference to related tour                    |
| Description       | String      | Brief description of the resource            |

### 14. Notifications
| Column Name       | Data Type   | Description                                  |
|-------------------|-------------|----------------------------------------------|
| NotificationID    | Integer     | Unique identifier for each notification      |
| CustomerID        | Integer     | Reference to the customer                    |
| Message           | String      | Notification message                         |
| DateSent          | Date        | Date when the notification was sent          |
| ReadStatus        | Boolean     | Read status of the notification              | 

## Conclusion
This schema defines the essential structure and components for managing a travel agency's operations through Google Sheets efficiently. Each sheet provides vital information that enhances customer interaction and operational management.
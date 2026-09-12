# Metro Ticket Generating System in ServiceNow

## 1. Project Overview

The **Metro Ticket Generating System** is a ServiceNow-based capstone project developed to simplify and digitize the metro ticket booking process.

The system allows passengers to select their **starting station, destination station, journey type, number of passengers, and payment mode**. It also supports fare calculation and generates a **digital QR ticket** for ticket verification.

The main purpose of the project is to reduce waiting time and manual effort while providing a simple and convenient metro ticket-booking process.

---

## 2. Project Objectives

- Digitize the metro ticket booking process using ServiceNow.
- Reduce passenger waiting time and manual ticketing effort.
- Provide easy selection of starting and destination stations.
- Support single and return journey options.
- Allow passengers to select the number of passengers.
- Calculate the ticket fare based on the selected journey details.
- Provide payment options such as UPI, Card, and Others.
- Generate digital metro tickets using QR codes.
- Reduce paper usage through digital ticketing.
- Improve the overall ticket-booking experience.

---

## 3. Stakeholders

- **Passengers** – Book metro tickets and receive digital tickets.
- **Station Managers** – Maintain metro station information.
- **Metro Operations Team** – Support metro ticketing operations.
- **System Administrators** – Configure and maintain the ServiceNow system.

---

## 4. Technologies and ServiceNow Features Used

- ServiceNow
- Service Catalog
- Custom Tables
- Catalog Item
- Catalog Variables
- Catalog Client Scripts
- JavaScript
- Service Portal
- QR Code Generation
- Access Control

---

## 5. Main Components

### 5.1 Metro Station Details

A custom ServiceNow table is used to store metro station information.

**Table:** `u_metro_station_s_details`

The station information is used for:

- Starting From
- Going To

### 5.2 Book A Metro Ticket

A ServiceNow Catalog Item is used to provide the metro ticket-booking form.

**Catalog Item:** `Book A Metro Ticket`

The booking form contains:

- Starting From
- Going To
- Type Of Journey
- No Of Passengers
- Amount For Single Journey
- Amount Including Return
- Mode Of Payment

### 5.3 Type Of Journey

Passengers can select:

- Single Journey
- Return Journey

### 5.4 Number Of Passengers

The system allows passengers to select:

- 1 Passenger
- 2 Passengers
- 3 Passengers
- 4 Passengers

### 5.5 Payment Mode

The available payment options are:

- UPI
- Card
- Others

### 5.6 Fare Calculation

The system calculates the ticket amount according to the selected journey details and number of passengers.

The calculated amount is displayed in the booking form.

### 5.7 QR Ticket

After the booking details are processed, a QR code is generated for the digital metro ticket.

The QR code can be used for ticket verification at the metro entry point.

### 5.8 Metro QR Widget

**Widget Name:** `Metro QR Widget`

**Widget ID:** `metro_qr_widget`

The widget is used to display the generated QR code and related ticket information.

---

## 6. Ticket Booking Process

```text
Passenger
    |
    v
Book A Metro Ticket
    |
    v
Select Starting Station
    |
    v
Select Destination Station
    |
    v
Select Journey Type
    |
    v
Select Number Of Passengers
    |
    v
Calculate Fare
    |
    v
Select Payment Mode
    |
    v
Generate QR Ticket
    |
    v
Display Digital Ticket
    |
    v
Ticket Verification

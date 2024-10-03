# Car Rental System

## Overview

This is a simple **Car Rental System** developed in Java that allows customers to rent and return cars. The system manages a list of available cars, allows customers to select a car for rental, and processes returns of rented cars.

The system is designed for console-based interaction, with a menu-driven interface where users can:
1. Rent a car.
2. Return a car.
3. Exit the system.

The system tracks the availability of cars and ensures that only available cars can be rented. When a car is returned, it becomes available for rental again.

## Features

- **Add Cars**: The system includes a set of predefined cars with details such as car ID, brand, model, and base price per day.
- **Add Customers**: When renting a car, a new customer is created and stored with a unique ID.
- **Rent Cars**: Customers can select a car to rent for a specified number of days, and the total rental price is calculated based on the daily rate.
- **Return Cars**: Customers can return rented cars, making them available again for future rentals.
- **Menu Interface**: The system provides a simple menu interface to guide users through the options.
  
## Classes

### 1. Car
This class represents a car available for rental.

- **Attributes**:
  - `carId`: Unique ID of the car.
  - `brand`: Brand of the car (e.g., Toyota).
  - `model`: Model of the car (e.g., Camry).
  - `basePricePerDay`: Daily rental rate for the car.
  - `isAvailable`: Boolean to track if the car is available for rental.

- **Methods**:
  - `calculatePrice(int rentalDays)`: Calculates the total rental price based on the number of days.
  - `isAvailable()`: Checks if the car is available for rent.
  - `rent()`: Marks the car as rented (i.e., unavailable).
  - `returnCar()`: Marks the car as returned (i.e., available).

### 2. Customer
This class represents a customer renting a car.

- **Attributes**:
  - `customerId`: Unique ID of the customer.
  - `name`: Name of the customer.

- **Methods**:
  - `getCustomerId()`: Returns the customer ID.
  - `getName()`: Returns the customer's name.

### 3. Rental
This class links a car to a customer for a specific rental period.

- **Attributes**:
  - `car`: The rented car.
  - `customer`: The customer who rented the car.
  - `days`: The number of days the car is rented for.

### 4. CarRentalSystem
This is the core system that manages car rentals and returns.

- **Attributes**:
  - `cars`: List of all cars available for rental.
  - `customers`: List of all customers who have rented cars.
  - `rentals`: List of all active rentals.

- **Methods**:
  - `addCar(Car car)`: Adds a car to the list of available cars.
  - `addCustomer(Customer customer)`: Adds a new customer to the system.
  - `rentCar(Car car, Customer customer, int days)`: Processes the car rental, marks the car as rented, and stores the rental information.
  - `returnCar(Car car)`: Marks the car as returned and removes the rental record.
  - `menu()`: Provides a menu interface for users to interact with the system.

## How to Use

1. **Run the Program**:
   Compile and run the `Main` class to start the Car Rental System. The system will present a menu with three options.

2. **Renting a Car**:
   - Choose the "Rent a Car" option.
   - Enter your name when prompted.
   - Select an available car from the list by entering the car ID.
   - Enter the number of days for the rental.
   - The system will display the total rental cost and ask for confirmation.
   - Confirm the rental by entering "Y" or cancel by entering "N".

3. **Returning a Car**:
   - Choose the "Return a Car" option.
   - Enter the car ID of the car you wish to return.
   - The system will process the return and mark the car as available for future rentals.

4. **Exiting the System**:
   - Choose the "Exit" option to close the program.

## Example

Below is an example interaction:

===== Car Rental System =====

Rent a Car
Return a Car
Exit Enter your choice: 1
== Rent a Car ==

Enter your name: John Doe

Available Cars: C001 - Toyota Camry C002 - Honda Accord C003 - Mahindra Thar

Enter the car ID you want to rent: C001 Enter the number of days for rental: 3

== Rental Information == Customer ID: CUS1 Customer Name: John Doe Car: Toyota Camry Rental Days: 3 Total Price: $180.00

Confirm rental (Y/N): Y

Car rented successfully.


## Car Details in the System

Here are the predefined cars in the system:

- **Car 1**: Toyota Camry (ID: C001) - $60.00 per day
- **Car 2**: Honda Accord (ID: C002) - $70.00 per day
- **Car 3**: Mahindra Thar (ID: C003) - $150.00 per day

## Dependencies

- **Java**: This program is written in Java and requires a Java Development Kit (JDK) to compile and run.

## Running the Program

1. Download the project.
2. Open the project in your preferred IDE (e.g., IntelliJ, Eclipse) or compile via terminal.
3. Run the `Main` class to start the Car Rental System.

```bash
javac Main.java
java Main

# BED Assignment 1

Back-End Web Development (BED) CA1 Assignment

Developed endpoints in the back-end for a flight booking website

# SQL TABLES CREATED
Database name: sp_air
- user - stores user information
    - user id
    - username
    - email
    - contact number
    - password
    - role
    - profile picture

- flight - stores flight information
    - flight id 
    - flight code
    - aircraft type
    - origin airport
    - destination airport
    - embark date
    - travel time
    - price
 
- airport - stores airport name and country
    - airport id
    - name of airport
    - country of airport
    - description of airport

- bookings - stores booking made by a user
    - booking id
    - name
    - passport
    - nationality
    - age

- promotion - store promotion period dates and discounts
    - promotion id
    - startDate
    - endDate
    - discount
    - flight id

## SUMMARY OF ENDPOINTS CREATED
1. Endpoint 1 - POST /users/ - Create a new user
2. Endpoint 2 - GET /users/ - Get all users from the user database
3. Endpoint 3 - GET /users/:id - Get user by their id
4. Endpoint 4 - PUT /users/:id - Update a user by their id
5. Endpoint 5 - POST /airport - Add a new airport
6. Endpoint 6 - GET /airport - Get all airports from the airport database
7. Endpoint 7 - POST /flight - Update airport information
8. Endpoint 8 - GET /flightDirect/:originAirportId/:destinationAirportId - Get flights travelling from origin airport to destination airport
9. Endpoint 9 - POST /booking/:userid/:flightid - Add a new booking to the booking database
10. Endpoint 10 - DELETE /flight/:id/ - Delete a flight by its id
11. Endpoint 11 - GET /transfer/flight/:originAirportId/:destinationAirportId - Get transfer flights to destination

# BONUS REQUIREMENTS FUFILLMENT
- Implementation of Multer in app.js to support uploading of image files into form-data in POSTMAN
    > - File size limited to 1MB, otherwise error will be outputted
    > - Only JPG and PNG files are accepted, using fileFilter function in Multer object and comparing with file mimetype
    > -  Feature is only available for user endpoints

- Endpoints related to promotional discounts for certain periods
    12. Endpoint 12 - POST /promotions/:flightid - Create a new promotion
    13. Endpoint 13 - GET /promotions - Get all promotions
    14. Endpoint 14 - GET /promotions/:promotionid - Get promotion by promotionid
    15. Endpoitn 15 - DELETE /promotion/:promotionid - Delete a promotion by promotionid

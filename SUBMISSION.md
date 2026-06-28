# Submission

## Selected Tasks

### 1. Create a basic booking endpoint

Create a basic booking endpoint
POST /api/bookings
Accept: client email, hairdresser ID, date, start time
Validate: required fields, email format, business rules (no weekends, business hours, one per hour)
Return JSON: success/error with clear messages

I read the task and I noticed that there are some incosistent things compared to the database(hairdresserId). So the first thing was to
ask if i get can more information to solve the task.

I didn't get any information so I made the decision to add a `HairDressers` table and link to the bookings through `bookings.hairdresser_id`

## Why I decided like this?

Usually in a Hairdresser Shop multiple haidressers are working. This way our website will stay flexible if we want to have multipe Hairdressers, make profiles for hairdressers or show personal calendar for them.

Added the `POST /api/bookings` endpoint

I modified the frontend to be consistent with the new logic, so now when you are making a reservation you need to choose a hairdresser

I checked if the logic works correctly with Postman

I wrote tests to check if the functinality was implemented correctly - api booking can be created  
 - same hairdresser cannot be double booked for same slot  
 - different hairdresser can be booked for same slot  
 - outside business hours booking is rejected

### 2. Create a basic booking endpoint

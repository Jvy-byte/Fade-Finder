# Fade Finder

## Table of Contents
- [Overview](#overview)
- [Product Spec](#product-spec)
- [Wireframes](#wireframes)

## Overview
### Description
The Fade Finder Barbershop App is a social networking app designed for individuals seeking a new haircut style or barber. Barbers can upload images of their work, and clients can swipe left or right based on their interest. Clients can also view barbers in three local areas of their choosing, making it easier to find someone nearby. The app aims to create a seamless experience for those looking for a fresh cut while giving barbers a platform to showcase their skills.

### App Evaluation
- **Category**: Social Networking / Lifestyle
- **Story**: Connects clients with barbers based on hairstyle preferences, allowing them to match, chat, and potentially book an appointment.
- **Market**: Suitable for anyone interested in finding a barber or new hairstyle, particularly people who like to try different looks and styles.
- **Habit**: The app can be used on a regular basis, depending on how often users are looking to change their hairstyle or find a new barber.
- **Scope**: Initially, the app will match clients with barbers based on hairstyle images. Eventually, it could expand to include booking options, reviews, and detailed barber profiles with specialties.

## Product Spec
### 1. User Stories (Required and Optional)

**Required Must-have Stories**
- User logs in to access saved styles and preferences.
- User browses different barbers and hairstyles in selected areas.
- Clients can swipe left or right on hairstyles posted by barbers, with a match feature for chatting.
- Profile pages for each barber, including photos of past work, pricing, and specialties.
- Settings page with options for notifications, account preferences, and language selection.

**Optional Nice-to-have Stories**
- Favorites list to save specific barbers and hairstyles.
- Booking feature to schedule appointments directly within the app.
- Profile page for clients to fill out personal preferences, hair type, and preferred hairstyle.
- Queue for saved matches or styles to view later.
- Option for barbers to post promotional discounts or special offers.

### 2. Screens

- **Login Screen**:
  - Users sign up or log in to access their profile and saved preferences.
  - Option to log in with email, Google, or Apple accounts.
  
- **Register Screen**:
  - New users can create an account, enter their basic info, and select local areas of interest.
  
- **Swipe Screen**:
  - Clients view hairstyle options posted by barbers and swipe left (dislike) or right (like) on each style.
  - If there’s a match, a chat window opens.
  
- **Chat Screen**:
  - Clients can chat directly with matched barbers to discuss styles, pricing, and availability.
  
- **Profile Screen (Barber)**:
  - Barbers can upload photos of their work, set their availability, and list their specialties.
  
- **Profile Screen (Client)**:
  - Clients can fill out a profile, including hair type, preferred styles, and contact preferences.
  
- **Settings Screen**:
  - Users can manage notifications, language settings, and app preferences.

### 3. Navigation

**Tab Navigation (Tab to Screen)**
- Swipe Screen
- Profile (Client / Barber)
- Settings

**Optional Tabs**
- Favorites (Saved Hairstyles / Barbers)
- Booking (Appointment Schedule)

**Flow Navigation (Screen to Screen)**

- Forced Login -> Account Creation if no login is available
- Swipe Screen -> Chat upon matching with a barber
- Profile -> Edit profile fields
- Settings -> Toggle app preferences


## Wireframes
![Wire Frame](https://github.com/Jvy-byte/Fade-Finder/blob/main/IMG_6753.jpg?raw=true)
![Wire Frame](https://github.com/BarberS-hop-App99/Fade-Finder/blob/main/Untitled%20design%20(1).png?raw=true)

# Fade Finder Data Models
![FadeFinder_1](https://github.com/user-attachments/assets/361fdae4-0c8a-47fa-a271-3068318a431a)


##### Barber API 

- Base URL - [https://api.got.show/api](https://api.got.show/api)

   HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    | /barbers | Retrieve a list of all barbers on the platform
    `GET`    | /barbers/:id | Retrieve a specific barber profile by :id
    `POST`    | /barbers   | Create a new barber profile
    `PUT`    | /barbers/:id |Update barber profile information by :id
    `DELETE`    | /barbers/:id |Update barber profile information by :id



   HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    | /users | Retrieve a list of all users on the platform
    `GET`    | /users/:id |Retrieve a specific user profile by :id
    `POST`    | /users  | Create a new user profile
    `PUT`    | /users/:id |Update user profile information by :id
    `DELETE`    | /users/:id |Delete a user profile by :id

     HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    | /swipes/:userId | Retrieve swipe history for a specific user by userId
    `POST`    | /swipes |Create a new swipe action (like or dislike)
    `GET`    | /matches/:userId |Retrieve matched barbers for a specific user by userId

     HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    |/appointments| Retrieve a list of all appointments
    `GET`    | /appointments/:userId| Retrieve appointments for a specific user by userId
    `POST`    | /appointments  | Create a new appointment
    `PUT`    | /appointments/:appointmentId |Update appointment details by appointmentId
    `DELETE`    | /appointments/:appointmentId |Cancel an appointment by appointmentId

     HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    |/barbers/nearby?lat=:lat&lng=:lng| Find barbers nearby based on latitude (lat) and longitude (lng)
    `GET`    | /barbers/:id/location| Get location information for a specific barber by :id

     HTTP Verb | Endpoint | Description
   ----------|----------|------------
    `GET`    | /barbers/:id/instagram | Retrieve Instagram profile link for a barber by :id
    `POST`    | /barbers/:id/instagram/connect	|Connect a barber’s Instagram account
    `DELETE`    | /barbers/:id/instagram/disconnect |Disconnect a barber’s Instagram account
    
   ## Build Progress
  As it comes to building out Fade Finder we are continuing to plan and execute all the details and steps within Fade Finder to make it a total and complete application, understanding this is essential. While working on the database schema for Fade Finders, the focus is on creating a well-structured and scalable foundation that efficiently stores and manages the app’s core data. Using Firebase as the backend, the database models are defined for key entities like Users, Appointments, Services, and Reviews. The Users collection includes both barbers and customers, with role-specific fields such as availability for barbers and booking history for customers. The Services collection lists the types of haircuts or grooming options offered, ensuring barbers can define their offerings and customers can make informed selections


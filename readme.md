# Jefe Compass - Public REST API

![Logo JEFE](./jefe.svg)

## Introduction
Welcome to the public documentation of the Jefe Compass REST API. This API provides access to various functionalities of Jefe Compass, including user registration and authentication. Use the JEFE COMPASS at <a href="https://app.jefetoken.com"> JEFE COMPASS WEB3 APP </a> or download for Android-linux based systems at: <a href="https://play.google.com/store/apps/details?id=com.jefetoken.jefecompass"> ANDROID JEFE COMPASS </a> 

### Base URL
The base URL for all requests is:

```
http://51.195.202.219:8010/api/public
```

## User Registration

Allows registering a new user in Jefe Compass.

- **URL:** `/users`
- **Method:** `POST`
- **Headers:** 
  - `Content-Type: application/json`
- **Request Body:**

```json
{
  "username": "string",
  "password": "string",
  "email": "string", 
  "wallet": "string", 
  "telegram": "string",
  "twitter": "string"
}
```

- **Successful Response:**
  - **Code:** 200 OK
  - **Response Body:** Authentication token
  
- **Request Example:**

```bash
curl -X POST http://51.195.202.219:8010/api/public/users \
     -H "Content-Type: application/json" \
     -d '{
          "username": "example",
          "password": "password123",
          "email": "example@example.com", 
          "wallet": "example_wallet_address", 
          "telegram": "@example",
          "twitter": "@example_twitter"
        }'
```

## Login

Allows a user to log in to Jefe Compass.

- **URL:** `/auth/login`
- **Method:** `POST`
- **Headers:** 
  - `Content-Type: application/json`
- **Request Body:**

```json
{
  "username": "string",
  "password": "string"
}
```

- **Successful Response:**
  - **Code:** 200 OK
  - **Response Body:** Authentication token
  
- **Request Example:**

```bash
curl -X POST http://51.195.202.219:8010/api/public/auth/login \
     -H "Content-Type: application/json" \
     -d '{
          "username": "example",
          "password": "password123"
        }'
```

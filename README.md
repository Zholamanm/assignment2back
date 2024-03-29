
---

# Assignment 2 - Weather and AQI Dashboard

## Description

This project is a web application that provides real-time weather information, air quality index (AQI), and a clock synchronized with the time of the selected city. It uses various APIs to fetch weather data, AQI, and city-specific time data.

## Features

- Real-time weather information for a selected city.
- Display of AQI data based on the location's latitude and longitude.
- A real-time clock that shows the current time in the selected city.

## Setup Instructions

### Prerequisites

- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository to your local machine.
    ```bash
    git clone [repository URL]
    ```
2. Navigate to the project directory.
    ```bash
    cd assignment2back
    ```
3. Install the required dependencies.
    ```bash
    npm install
    ```

### Running the Application

1. Start the server.
    ```bash
    npm start
    ```
2. Open a web browser and navigate to `http://localhost:3000`.

## API Usage

### Weather API

- **Endpoint**: `/api/weather/:city`
- **Method**: GET
- **Description**: Fetches the weather data for the specified city.
- **Parameters**:
    - `city`: Name of the city.

### AQI API

- **Endpoint**: `/api/aqi/:lat/:lon`
- **Method**: GET
- **Description**: Fetches the AQI data based on latitude and longitude.
- **Parameters**:
    - `lat`: Latitude of the location.
    - `lon`: Longitude of the location.

### City Time API

- **Endpoint**: `/api/city/:name`
- **Method**: GET
- **Description**: Fetches the current time data for the specified city.
- **Parameters**:
    - `name`: Name of the city.

## Key Design Decisions

### Frontend Logic

- The application's frontend is designed to interact with the backend APIs to fetch and display data dynamically.
- JavaScript is used for handling user interactions and updating the DOM with the received data.
- A modular approach is followed for separate functionalities like fetching weather data, AQI, and city time.

### Backend Server

- The server is built using Express.js, a fast, unopinionated, minimalist web framework for Node.js.
- CORS (Cross-Origin Resource Sharing) is enabled to allow requests to the API from the frontend.
- Environment variables are used to store API keys securely.

## Dependencies

- `express`: Web application framework for Node.js.
- `axios`: Promise-based HTTP client for making HTTP requests.
- `cors`: Middleware to enable CORS.
- `dotenv`: Module to load environment variables from a `.env` file.
- `request`: Simplified HTTP request client.

---
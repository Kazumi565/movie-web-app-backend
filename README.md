Movie Review Web App - Backend (Spring Boot)
============================================

This repository houses the backend code for my movie review web application. It's built using Spring Boot and MongoDB, providing robust RESTful APIs to handle everything related to movies and reviews.

Table of Contents
-----------------

*   [Prerequisites](#prerequisites)
    
*   [Installation](#installation)
    
*   [Configuration](#configuration)
    
*   [Usage](#usage)

*   [Import Movie Data](#import-movie-data)
    
*   [Contributing](#contributing)
    

Prerequisites
-------------

To get started, make sure you have the following installed:

*   **Java Development Kit (JDK):** Version 8 or later is required.
    
*   **Spring Boot:** You can use either the Spring Boot CLI or your favorite IDE that supports Spring Boot development (I recommend IntelliJ IDEA or Eclipse).
    
*   **MongoDB:** You'll need a MongoDB database instance. You can set one up locally or opt for a cloud-based solution like MongoDB Atlas.
    

Installation
------------

1. **Clone the repository:**

  ```bash
    git clone
  ```
2. **Navigate to the project directory:**
  ```bash
    cd movie-review-app-backend
  ```
3. **Open in your IDE:** Import the project into your chosen IDE.
    

Configuration
-------------

1. **Create a `.env` file:**

  In the root directory of your project, create a file named `.env`. This is where you'll store your sensitive database credentials, keeping them separate from your code. Add the following lines, replacing the placeholders with your actual MongoDB information:
```bash
MONGO_DATABASE=<your-database-name>
MONGO_USER=<your-mongodb-username>
MONGO_PASSWORD=<your-mongodb-password>
MONGO_CLUSTER=<your-mongodb-cluster-name>
```
2. **Update `application.properties`:**
   
 Make sure your `application.properties` file (inside `src/main/resources`) looks like this:
```bash
spring.application.name=movies
spring.data.mongodb.database=${env.MONGO_DATABASE}
spring.data.mongodb.uri=mongodb+srv://${env.MONGO_USER}:${env.MONGO_PASSWORD}@${env.MONGO_CLUSTER}
```
Usage
-----
1. **Build the project:**
   
   Within your IDE or via your terminal, run this command to build everything:
```basg
./mvnw clean install
```
2. **Run the application:**
   
   You have two options here:
    By default, the application should start on port 8080.
    
    *   **IDE:** Hit that "Run" button directly in your IDE.
        
    *   **Terminal:** Use the command line:
```bash
./mvnw spring-boot:run
```
Import Movie Data
-----------------

1.  **Locate JSON File:** Open the `movie\_data` folder in this repository. You'll find a JSON file `movies.json` containing the movie data.
    
2.  **Open MongoDB Compass:** Connect to your MongoDB database using MongoDB Compass.
    
3.  **Select Collection:** Select the movies collection in your database.
    
4.  **Import Data:**
    
    *   Click the "Add Data" button, then choose "Import File."
        
    *   Select the JSON file from the movie\_data folder.
        
    *   Choose "JSON" as the file type and click "Import."
      
Contributing
------------

Feel free to fork the repository and submit pull requests if you'd like to contribute!

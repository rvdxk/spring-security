
# Spring Boot Security with Authentication Controller
This project demonstrates the implementation of Spring Security in a Spring Boot application with a focus on creating a simple authentication system. The authentication is done through a POST request to the endpoint /api/v1/auth/authenticate, and once authenticated, a token is generated for subsequent requests.

## Prerequisites
-IDE (Integrated Development Environment) for running the Spring Boot application.
-Postman for testing the authentication and authorization.

## Getting Started
1. Clone the Repository:
-git clone <[repository_url](https://github.com/rvdxk/spring-security)>
2. Open in IDE:
-Open the project in your preferred IDE.
3. Run the Application:
-Run the Spring Boot application to start the server.
4. Testing Authentication:
-Open Postman and send a POST request to http://localhost:8080/api/v1/auth/authenticate with the following JSON payload in the raw body:
<pre>
  json
{
    "email": "admin@gmail.com",
    "password": "admin"
}
</pre>
This will return an authentication token. Copy the token for further use.
5. Testing Authorization:

-Make a GET request to http://localhost:8080/api/v1/greetings without any authorization. This should result in an unauthorized response.
-Set up authorization in Postman by selecting the "Bearer Token" type and pasting the copied token. Now, make the same GET request to http://localhost:8080/api/v1/greetings. This should return a successful response.
-Similarly, test the endpoint http://localhost:8080/api/v1/greetings/say-good-bye with the authorized token.

## Endpoints

Authentication:

- Endpoint: POST /api/v1/auth/authenticate
- Payload:
<pre>
json
{
    "email": "admin@gmail.com",
    "password": "admin"
}
</pre>
- Greetings:

- Endpoint: GET /api/v1/greetings

- Authorization: Bearer Token required

- Endpoint: GET /api/v1/greetings/say-good-bye

- Authorization: Bearer Token required

Important Notes
Ensure that your IDE and Postman are set up and running.
Feel free to explore and extend this project to suit your authentication and authorization needs. Happy coding!







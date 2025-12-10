Understanding Security Requirements: The necessity of securing API endpoints is discussed, highlighting the security risks of leaving them accessible without authentication.

Spring Security Dependency: The session begins with adding the Spring Security dependency, explaining its importance in enforcing security measures within the project.

Setting Up In-Memory Users: Instructions on creating in-memory users with different roles (admin and regular user) are provided, including how to configure these roles for security settings.

Configuring Security Rules: The lecture details how to define authorization rules for various API endpoints, differentiating access for users and admins, and specifying public endpoints not requiring authentication.

Testing the API: Emphasis is placed on testing the API using tools like Postman, ensuring that the security implementations are functioning properly.

Handling Common Issues: Common issues, including password encoding errors and CSRF protection, are addressed with solutions to ensure the API operates correctly.

Final Testing and Validation: The session concludes with comprehensive tests to validate the correct implementation of security configurations based on user roles and authentication status.

# CURL Requests

### 1. Create a Customer

```bash
curl -X POST http://localhost:8080/api/customers \
  -H "Content-Type: application/json" \
  -d '{
        "firstName": "John",
        "lastName": "Doe",
        "email": "john.doe@example.com",
        "phoneNumber": "1234567890"
      }'
```

---

### 2. Get All Customers

```bash
curl -X GET http://localhost:8080/api/customers
```
---

### 3. Get Customer by ID

```bash
curl -X GET http://localhost:8080/api/customers/1
```

---

### 4. Update a Customer

```bash
curl -X PUT http://localhost:8080/api/customers/1 \
  -H "Content-Type: application/json" \
  -d '{
        "firstName": "Jane",
        "lastName": "Smith",
        "email": "jane.smith@example.com",
        "phoneNumber": "9876543210"
      }'
```

---

### 5. Delete a Customer

```bash
curl -X DELETE http://localhost:8080/api/customers/1
```

# Spring Boot RabbitMQ Demo
A Spring Boot project demonstrating RabbitMQ integration for efficient asynchronous communication through RESTful web services

## Steps to Setup

**1. Pull RabbitMQ Image**

```bash
docker pull rabbitmq:3.10.25-management
```

**2. Run RabbitMQ in a Container**

Run a RabbitMQ container using the pulled image:
```bash
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:3.10.25-management
```

This command starts a RabbitMQ container, exposes the default ports 5672 (AMQP) and 15672 (management UI)

**3. Clone the Application**

```bash
git clone https://github.com/attrayadas/springboot-rabbitmq-demo
```

**4. Run the Spring Boot Application**

Run the Spring Boot application using the following command:
```bash
mvn spring-boot:run
```

**5. Send a Message using GET and POST Requests**

Use Postman to send GET and POST requests to the endpoints in your Spring Boot application

```bash
GET http://localhost:8080/api/v1/publish?message=hello
```

```bash
POST http://localhost:8080/api/v1/publish
Content-Type: application/json

{
    "id": 2,
    "firstName": "Attraya",
    "lastName": "Das"
}
```

**6. Check Logs for Message Sent and Received**

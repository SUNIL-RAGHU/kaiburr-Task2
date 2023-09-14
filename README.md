# Kaiburr-Task-2

# 

Task 2. Swagger codegen.
Create the same REST API as in task #1, but use [https://editor.swagger.io/](https://editor.swagger.io/) to create your API definition and generate the server code. Choose any java-based server or server framework, that you like. You can either use the online editor or generate the code manually, e.g. using this document: [https://github.com/swagger-api/swagger-codegen/wiki/server-stub-generator-howto](https://github.com/swagger-api/swagger-codegen/wiki/server-stub-generator-howto). Make sure that you can deploy/run the generated code. Once your stub is ready - implement the same functionality as described in task #1, but now in java.
Finally, be sure that you can show how your application responds to requests using postman, curl or any other HTTP client.

## **Prerequisites**

- Docker installed on your system
- Git installed on your system

## **Setup**

### **Step 1: Pull the latest MongoDB image**

```bash
docker pull mongo:latest
```

### **Step 2: Clone the repository**

```bash
git clone <repository_url>
```

### **Step 3: Navigate to the repository**

```bash
cd <repository_directory>
```

### **Step 4: Build the Docker image for the Spring Boot application**

```bash
docker build -t kaiburr-api .
```

### **Step 5: Open the terminal and navigate to `src/resources`**

```bash
cd src/resources
```

### **Step 6: Start the Docker Compose to run MongoDB and the Spring Boot application**

```bash
docker-compose up
```

### ****API Endpoints****

[**http://localhost:9090/swagger-ui/index.html#/**](http://localhost:9090/swagger-ui/index.html#/)

## **`GET /servers/get`**

### **Description**

This endpoint retrieves a list of servers.

### **Request**

- Method: GET
- URL: [http://localhost:9090/swagger-ui/index.html#/server-controller/getAllServers](http://localhost:9090/swagger-ui/index.html#/server-controller/getAllServers)

### 

## **`POST /servers/create`**

### **Description**

This endpoint adds a new server.

### **Request**

- Method: POST
- URL: [http://localhost:9090/swagger-ui/index.html#/server-controller/createServer](http://localhost:9090/swagger-ui/index.html#/server-controller/createServer)
- Body: JSON Object

### 

## **`DELETE /servers/{id}`**

### **Description**

This endpoint deletes a server.

### **Request**

- Method: DELETE
- URL: [http://localhost:9090/swagger-ui/index.html#/server-controller/deleteServer](http://localhost:9090/swagger-ui/index.html#/server-controller/deleteServer)
- Path Variable: **`id`** (ID of the server to delete)

### 

## **`GET /servers/findbyname?name={name}`**

### **Description**

Retrieves a server by its name.

### **Request**

- Method: GET
- URL: [http://localhost:9090/swagger-ui/index.html#/server-controller/findServersByName](http://localhost:9090/swagger-ui/index.html#/server-controller/findServersByName)
- Path Variable: **`name`** (Name of the server)

###
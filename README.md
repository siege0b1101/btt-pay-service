# BTT Pay Service

BTT Pay Service serves as the backend service for BTT Pay application. This project is made for Big Trading Traders built using Spring Boot, Spring Security, and Spring Data JPA.

## Setup (macOS)

For easier setup, I recommend using Homebrew to manage all related tools and environment.

### 1. Install Homebrew
Refer to https://brew.sh

### 2. Java (25)
```
brew install openjdk@25
```

### 3. Maven (3.9.xx)
```
brew install maven
```

### 4. PostgreSQL
1. Install via homebrew
```
brew install postgresql@18
```

2. Start PostgreSQL  
```
brew services start postgresql@18
```  
> [!WARNING]
> To stop PostgreSQL  
> ```
> brew services stop postgresql@18
> ```

3. Create default user  
```
psql postgres
CREATE ROLE postgres WITH LOGIN PASSWORD '<password>';
ALTER ROLE postgres WITH LOGIN CREATEDB CREATEROLE SUPERUSER;
\q
```

4. Create database  
```
psql -U postgres
CREATE DATABASE btt_pay;
```

5. Verify database creation  
```
\l
```

### 5. Run  
1. Run the server  
```
mvn spring-boot:run
```

2. Verify via Swagger UI  
http://localhost:8080/swagger-ui/index.html
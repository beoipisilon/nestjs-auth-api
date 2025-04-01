# NestJS Auth API  

A simple authentication API using **NestJS, PostgreSQL, and JWT**.  

## Features  

- User registration and login  
- Authentication with **JWT + Refresh Token**  
- Protected routes  
- PostgreSQL with **TypeORM**  

## Setup  

1. Clone the repo and install dependencies:  
   ```bash
   git clone https://github.com/beoipisilon/nestjs-auth-api.git  
   cd nestjs-auth-api  
   npm install  
   ```  

2. Create a `.env` file:  
   ```env
    DATABASE_URL=postgresql://username:password@localhost:5432/auth_db  
    JWT_SECRET=your_jwt_secret  
    JWT_REFRESH_SECRET=your_refresh_token_secret  
    JWT_EXPIRATION=15m
    JWT_REFRESH_EXPIRATION=7d
    PORT=3000
    ```  

3. Run database migrations:  
   ```bash
   npm run typeorm migration:run  
   ```  

4. Start the app:  
   ```bash
   npm run start:dev  
   ```  

## API Endpoints  

- **POST** `/auth/register` – Register user  
- **POST** `/auth/login` – User login  
- **POST** `/auth/refresh` – Refresh token  
- **GET** `/users/me` – Get user profile
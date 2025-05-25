# GraphQL Task Implementation
This guide walks you through the process of setting up, implementing, and testing the GraphQL task from cloning the repository to verifying the solution.

## Steps to Get Started
### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/nadyavalin/rsschool-nodejs-task-graphql.git
```
```bash
cd rsschool-nodejs-task-graphql
```
### 2. Install Dependencies
Install the project dependencies using npm:
```bash
npm ci
```

### 3. Set Up Environment Variables
Create `.env` file (based on `.env.example`): `./.env`

### 4. Set Up the Database
The project uses SQLite with Prisma.
Create the database file and apply migrations:
```bash
npx prisma migrate deploy
```

### 5. Start the Server
Run the server to test the GraphQL endpoint locally:
```bash
npm run start
```
The server runs on `http://127.0.0.1:8000` or `http://[::1]:8000`.
Access the GraphQL endpoint at `http://[::1]:8000/graphql` using a tool like Postman.
You can watch documentation at `http://[::1]:8000/docs`

To check the task you needn't launch the server. Press `Ctrl + C`.

### 6. Test the Implementation 
Ensure the database is reset before testing:
```bash
npx prisma migrate reset
```
Make sure the important files have not been changed:
```bash
npm run test-integrity
```

Then launch the tests one by one:
```bash
npm run test-queries
```
```bash
npm run test-mutations
```
```bash
npm run test-rule
```
```bash
npm run test-loader
```
```bash
npm run test-loader-prime
```

Thank you for checking my work!
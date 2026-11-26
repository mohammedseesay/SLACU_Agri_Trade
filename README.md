# SLACU Agri-Trade Platform

Academic web prototype for AgriTech Solutions SL / Sierra Leone Agricultural Cooperative Union.

## Technology
- Windows 11 development environment
- Node.js and Express.js backend
- PostgreSQL database
- HTML, CSS and browser JavaScript frontend
- Session-based authentication and bcrypt password hashing

## 1. Requirements
Install Node.js LTS, PostgreSQL (including pgAdmin 4), and Visual Studio Code.

## 2. Configure
1. Open this folder in VS Code.
2. Copy `.env.example` and rename the copy to `.env`.
3. Edit `.env`; set your PostgreSQL password and a long random SESSION_SECRET.
4. Do not upload `.env` to GitHub.

## 3. Install packages
Open Terminal > New Terminal in VS Code and run:
```bash
npm install
```

## 4. Create database
Create a PostgreSQL database named `slacu_agri_trade` in pgAdmin.
Open Query Tool for that database, open `database/schema.sql` in VS Code, copy all SQL, paste it into Query Tool and press Execute (lightning icon).

## 5. Create demo administrator
In the VS Code terminal:
```bash
npm run seed
```
Demo login:
- Email: admin@slacu.local
- Password: ChangeMe123!

Change the demo password before any use beyond a classroom demonstration. The prototype currently seeds one administrator; additional role-specific user creation should be implemented and tested before real deployment.

## 6. Run
```bash
npm run dev
```
Open http://localhost:3000 in your browser. Stop the server with Ctrl+C.

## 7. Main modules
Dashboard, farmers, produce, market prices, buyers, orders, reports and audit logging.

## 8. Current prototype limitations
- SMS and USSD gateways are not connected.
- Offline-first capture and synchronisation are not implemented.
- No real payment integration, transport management or public deployment.
- Authentication uses session cookies; production deployment requires HTTPS, a strong secret, secure cookie configuration, backup procedures, access-control review and security testing.
- The initial prototype provides create/list workflows for core records; edit/delete workflows and self-service user administration are future enhancements.

## 9. Suggested test sequence
1. Log in with the demo administrator.
2. Register a farmer.
3. Register a buyer.
4. Add produce for the farmer.
5. Publish a market price.
6. Create an order using the buyer and produce.
7. Change the order status.
8. Download the farmers CSV report.
9. Sign out and confirm protected pages require login.

Use only fictional demonstration data in screenshots and presentations.

# A full-stack OTP (One-Time Password) email verification system

This project is a full-stack web application designed to handle One-Time Password (OTP) verification via email. It provides a secure way to authenticate users by sending a unique code to their email address and verifying it on the client side. The application features a robust Express.js backend integrated with SendGrid for email delivery, and a fast, responsive React frontend built with Vite and Tailwind CSS.

## Tech Stack

### Frontend (Client)
- **React 19**
- **TypeScript**
- **Vite**
- **Tailwind CSS 4**
- **React Router**

### Backend (Server)
- **Node.js**
- **Express.js**
- **SendGrid API** (`@sendgrid/mail`)
- **dotenv** & **cors**

## Prerequisites

Before you begin, ensure you have the following installed and set up:
- **Node.js** (v18 or higher recommended)
- **npm** (or your preferred package manager)
- A **SendGrid** account and API key for email delivery

## Local Setup and Installation

To run this project locally, you will need to set up and run both the server and the client in separate terminal windows.

### 1. Clone the repository

```bash
git clone <repository-url>
cd <repository-name>
```

### 2. Server Setup

Open a terminal and navigate to the `server` directory:

```bash
cd server
```

Install dependencies:

```bash
npm i
```

Configure environment variables:
Create a `.env` file in the `server` directory using the provided example.

```bash
cp .env.example .env
```
Edit the `server/.env` file with your SendGrid API key and sender details:
```env
PORT_NUMBER=5000
SENDGRID_API_KEY=SG.API_KEY_HERE
FROM_EMAIL=youremail@example.com
FROM_NAME=Your Name
```

Start the server:
```bash
node index.js
```
*(The server should now be running on `http://localhost:5000`)*

### 3. Client Setup

Open a new terminal window and navigate to the `client` directory:

```bash
cd client
```

Install dependencies:

```bash
npm i
```

Configure environment variables:
Create a `.env` file in the `client` directory using the provided example.

```bash
cp .env.example .env
```
Ensure the `client/.env` file points to your local server:
```env
VITE_API_URL=http://localhost:5000
```

Start the development server:
```bash
npm run dev
```
*(The client will typically start on `http://localhost:5173` - check your terminal output)*

## License

This project is licensed under the ISC License. See the `LICENSE` file for details.

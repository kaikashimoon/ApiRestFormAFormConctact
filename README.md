# Express Server with Nodemailer

This project sets up an Express server that uses Nodemailer to send emails. It includes the use of environment variables and support for CORS.

## Requirements

- Node.js
- npm (Node Package Manager)

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/your-username/nodemailer-express.git
    cd nodemailer-express
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Create a `.env` file in the root of the project and configure the following environment variables:

    ```env
    PORT=5000
    MAIL_USERNAME=your_email@domain.com
    MAIL_PASSWORD=your_password
    MAIL_HOST=smtp.office365.com
    MAIL_PORT=587
    MAIL_USER=recipient@domain.com
    ```

## Usage

To start the server, use the following command:

```bash
npm start
```

The server will listen on the port defined in the .env file or port 5000 by default.

### Endpoint: POST /api/v1/contact

**Description:**  
Sends an email with the provided data.

**URL:**  
`/api/v1/contact`

**Method:**  
`POST`

**Request Body:**

```json
{
  "name": "Sender's name",
  "email": "Sender's email",
  "number": "Sender's phone number",
  "text": "Sender's message"
}
```

**Success Response:**

```json
{
  "message": "Message sent successfully!"
}
```

**dotenv** is used to manage environment variables.
**express** is configured to handle JSON and URL-encoded requests.
**cors** is configured to allow requests from any origin.
**nodeMail** is used to send emails with the contact form details.
The **/v1/contact** endpoint receives the form data and uses mainMail to send the email.
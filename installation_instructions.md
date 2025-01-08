# VocalHost.ai - Installation Instructions

## Pre-Installation Steps

Before you begin the installation process, ensure you have the following:

1.  **Node.js and npm:** Make sure you have Node.js and npm installed on your system. You can download them from [nodejs.org](https://nodejs.org/).
2.  **Clover Developer Account:** You need a Clover developer account to integrate with the Clover API. If you don't have one, you can create it at [clover.com/developers](https://www.clover.com/developers).
3.  **API Credentials:**
    -   **Clover API Key:** Obtain your Clover API key from your Clover developer account.
    -   **Database Credentials:** You will need credentials for your database (e.g., username, password, host).
4.  **Webhook URL:** If you plan to use webhooks, you need a publicly accessible URL where webhook notifications will be sent.
5.  **Environment Variables:** Set up the following environment variables:
    -   `CLOVER_API_KEY`: Your Clover API key.
    -   `DATABASE_URL`: Your database connection string.
    -   `WEBHOOK_URL`: Your webhook URL.
    -   `JWT_SECRET`: A secret key for JWT authentication.
    -   `NEXTAUTH_SECRET`: A secret key for NextAuth.js.
    -   `NEXTAUTH_URL`: The URL of your application.

## Installation Steps

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/paulbugzy/VocalHost.ai.git
    cd VocalHost.ai
    ```
2.  **Navigate to the Frontend Directory:**
    ```bash
    cd crm-setup-frontend
    ```
3.  **Install Dependencies:**
    ```bash
    npm install
    ```
4.  **Set Environment Variables:**
    -   Create a `.env.local` file in the `crm-setup-frontend` directory.
    -   Add the environment variables you set up in the pre-installation steps to this file.
    ```
    CLOVER_API_KEY=your_clover_api_key
    DATABASE_URL=your_database_connection_string
    WEBHOOK_URL=your_webhook_url
    JWT_SECRET=your_jwt_secret
    NEXTAUTH_SECRET=your_nextauth_secret
    NEXTAUTH_URL=http://localhost:3007
    ```
5.  **Start the Development Server:**
    ```bash
    npm run dev
    ```
6.  **Access the Application:**
    -   Open your browser and navigate to `http://localhost:3007`.

## Post-Installation Steps

1.  **Database Setup:**
    -   Ensure your database is set up and accessible.
    -   Run any necessary database migrations or schema setup scripts.
2.  **Clover Configuration:**
    -   Configure your Clover app with the necessary permissions and settings.
    -   Test the Clover API connection.
3.  **Webhook Configuration:**
    -   Set up your webhook endpoint to receive notifications.
    -   Test the webhook functionality.

By following these instructions, you should be able to successfully install and run the VocalHost.ai platform.

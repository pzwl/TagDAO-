# TagDAO

TagDAO is a decentralized data labeling platform built on Web3 principles. It provides a crowdsourced marketplace for labeling tasks, integrated with crypto payments (using Solana) and secure file han[...]

## Overview

This platform allows requesters to create labeling tasks, set rewards in cryptocurrency, and manage data uploads securely. Workers can then label data and receive crypto payments upon completion. The [...]

- **Web3 Integration**: Leveraging Solana for transactions and payments.
- **Secure File Handling**: Using AWS S3 with pre-signed URLs to manage file uploads and downloads.
- **ML Support**: Providing a framework for tasks involving machine learning data, such as image or text labeling.
- **Security Best Practices**: Protecting private keys, validating on-chain transactions, and mitigating double-spend vulnerabilities.
- **Scalable Architecture**: Backend services for authentication (JWT), database management, and robust frontend components for both requesters and workers.

## Project Structure


### Technologies Used

- **Solana Web3.js** for blockchain interactions and payments
- **Node.js / Express** for backend services (API, authentication, database management)
- **React** for frontend interfaces (both user-facing and worker-facing)
- **AWS S3** for secure storage of user-uploaded assets using pre-signed URLs
- **JWT** (JSON Web Tokens) for authentication
- **Database** (e.g., MongoDB, PostgreSQL, or another) for storing user data, tasks, and transaction records
- **CDN** for efficient data distribution of assets globally

## Installation

1. **Clone the Repository**

    ```bash
    git clone https://github.com/pzwl/TagDAO-.git
    cd TagDAO-
    ```

2. **Install Dependencies for Each Directory**

    **Backend**:
    ```bash
    cd backend
    npm install
    ```
    *(or `yarn install` if you use Yarn)*

    **User Frontend**:
    ```bash
    cd ../user-frontend
    npm install
    ```
    *(or `yarn install` if you use Yarn)*

    **Worker Frontend**:
    ```bash
    cd ../worker-frontend
    npm install
    ```
    *(or `yarn install` if you use Yarn)*

3. **Configure Environment Variables**
    - Create a `.env` file in the `backend` folder for environment variables (e.g., database connection string, AWS credentials, Solana key, etc.).
    - Ensure your frontends have the correct environment variables for connecting to the backend and Solana network.

## Usage

1. **Start the Backend**

    ```bash
    cd backend
    npm run dev
    ```
    The backend will run at `http://localhost:5000` (or another configured port).

2. **Run the User Frontend**

    ```bash
    cd ../user-frontend
    npm start
    ```
    Access it in your browser at `http://localhost:3000`.

3. **Run the Worker Frontend**

    ```bash
    cd ../worker-frontend
    npm start
    ```
    Access it in your browser at `http://localhost:3001`.

4. **Interacting with Solana**
    - Update the Solana cluster URL (e.g., devnet, testnet, mainnet) and wallet details in your environment variables.
    - Ensure the private key is securely managed (avoid storing it directly in code or public repos).

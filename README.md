Bistro Boss Server
Welcome to the Bistro Boss Server, the backend for the Bistro Boss restaurant management system. This robust REST API, built with Node.js, Express, and MongoDB, powers a full-stack web application that streamlines restaurant operations, including menu management, user authentication, payment processing, and analytics. Integrated with Firebase, Stripe, and JWT for secure and efficient functionality, this server supports both user and admin features for an enhanced dining experience.
🚀 Features

User Authentication: Secure JWT-based authentication with role-based access control (admin/user).
Menu Management: CRUD operations for menu items with admin-only access for adding, updating, and deleting.
Cart Management: Add, retrieve, and delete cart items for users.
Payment Processing: Secure payment intents and transaction recording using Stripe.
Analytics: Admin endpoints for revenue, user, and order statistics with MongoDB aggregation.
Reviews: Fetch customer reviews for display in the frontend.
Secure API: Token-based authorization with middleware for protected routes.
CORS Support: Cross-Origin Resource Sharing for seamless frontend-backend communication.

🛠️ Technologies Used

Node.js & Express: For building a fast and scalable REST API.
MongoDB: For storing users, menu items, carts, payments, and reviews.
Stripe: For secure payment processing.
JSON Web Tokens (JWT): For secure user authentication and authorization.
MongoDB Atlas: For cloud-hosted database management.
Vercel: For easy deployment and hosting.
CORS: For enabling cross-origin requests.
dotenv: For managing environment variables.

📂 Project Structure
bistro-boss-server/
├── index.js                 # Main entry point for the server
├── .env                     # Environment variables (MongoDB URI, JWT secret, Stripe key)
├── package.json             # Project dependencies and scripts
├── README.md                # Project documentation

🖥️ Installation & Setup
Prerequisites

Node.js (v16 or higher)
MongoDB Atlas account or local MongoDB instance
Stripe account for payment processing
Vercel account for deployment (optional)

Steps

Clone the Repository:
git clone https://github.com/RejwanulIslam/bistro-boss-server.git
cd bistro-boss-server


Install Dependencies:
npm install


Set Up Environment Variables:Create a .env file in the root directory and add the following:
PORT=5000
DB_USER=your_mongodb_username
DB_PASS=your_mongodb_password
ACCESS_TOKEN_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key


Run the Server:
npm start

The server will be available at http://localhost:5000.

Frontend Setup:

Clone the frontend repository:git clone https://github.com/RejwanulIslam/bistro-boss-client.git
cd bistro-boss-client


Follow the setup instructions in the frontend README.
Ensure the frontend is configured to communicate with the backend (https://bistro-boss-server-tau-puce.vercel.app).



🌐 Live Demo

Backend API: https://bistro-boss-server-tau-puce.vercel.app
Frontend Application: https://bistro-boss-233c4.web.app

📚 API Endpoints
Authentication

POST /jwt: Generate a JWT token for a user.
GET /user/admin/:email: Check if a user is an admin (requires JWT).

Users

POST /users: Create a new user (checks for existing users).
GET /users: Retrieve all users (admin-only, requires JWT).
DELETE /users/:id: Delete a user by ID (admin-only, requires JWT).
PATCH /user/admin/:id: Promote a user to admin (admin-only, requires JWT).

Menu

GET /menu: Retrieve all menu items.
GET /menu/:id: Retrieve a specific menu item by ID.
POST /menu: Add a new menu item (admin-only, requires JWT).
PATCH /menu/:id: Update a menu item by ID (admin-only).
DELETE /menu/:id: Delete a menu item by ID (admin-only, requires JWT).

Carts

POST /carts: Add an item to a user's cart.
GET /carts?email=:email: Retrieve a user's cart items.
DELETE /carts/:id: Remove an item from a user's cart.

Payments

POST /create-payment-intent: Create a Stripe payment intent.
POST /payment: Save payment information and clear cart.
GET /payment/:email: Retrieve payment history for a user (requires JWT).

Reviews

GET /reviews: Retrieve all customer reviews.

Analytics

GET /admin-stats: Retrieve admin statistics (users, menu items, orders, revenue; admin-only, requires JWT).
GET /order-stats: Retrieve order statistics by category (admin-only, requires JWT).


🤝 Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add your feature').
Push to the branch (git push origin feature/your-feature).
Open a pull request.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.
📬 Contact
For any inquiries or feedback, reach out to:

GitHub: [RejwanulIslam](https://github.com/RejwanulIslam)
Email: rejwanul96@gmail.com


Thank you for exploring the Bistro Boss Server!This backend powers a seamless restaurant management experience, integrated with the Bistro Boss Client.
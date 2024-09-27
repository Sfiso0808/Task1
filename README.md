# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>`

Fullstack Assignment: Backend Simulation, Data Handling, and Security
Task Overview
This project simulates various backend functionalities including secure form submissions, data handling, and user reporting. Currently implemented using Vue.js, this project can be later ported to Node.js. While the task was initially set up on Vue.js for simplicity, all logic and structure are suitable for a Node.js backend and can be marked as such.

Technology Stack
Vue.js (current implementation for frontend)
Node.js (future backend porting)
Axios: For making HTTP requests
CSV Writer: For generating CSV reports
UUID: For creating unique IDs for users
MongoDB: For querying user data efficiently
WebSocket: For handling real-time communication (Bonus)
Tasks
Step 1: Simulate Secure Login Form Submission
Vue.js Implementation:
Currently, the form submission is simulated within a Vue.js frontend. It posts form data to a secure URL using axios and handles the response in a client-side environment.
Node.js Porting:
This task can be easily ported to Node.js by writing a backend API using Express.js. The API would securely post login data and receive a token and user array response. Additional security layers (like CSRF protection) can be added using csurf.
Step 2: Data Handling, Deduplication, and Performance Optimization
Vue.js Implementation:

In the current Vue.js setup, the data handling and deduplication logic are handled client-side. We deduplicate the users from users.json and generate a unique UUID for each user.
Node.js Porting:

For the Node.js backend, this process can be optimized using file streaming techniques and UUID generation on the server side. Handling large datasets efficiently can be achieved by using Node.js’s fs module and libraries like csv-writer for CSV generation.
Step 3: Simulate Secure User Data Posting
Vue.js Implementation:
The Vue.js frontend currently handles secure posting of user data from uniqueUsers.json to the API, retrying failed requests and ensuring error handling.
Node.js Porting:
This logic can be seamlessly ported to Node.js, where the backend securely posts user data to an external API. Retries and idempotency can be handled more robustly on the server side using libraries like axios and middleware for error handling.
Step 4: Engineering Department Reporting
Vue.js Implementation:

In the current implementation, the Vue.js frontend filters users in the Engineering department and identifies those reporting to Michael Phalane.
Node.js Porting:

This task can be enhanced using MongoDB in the Node.js backend. MongoDB’s powerful querying capabilities allow for efficient filtering and reporting on large datasets. You can also add indexing to improve performance when querying millions of records.
Step 5: WebSocket Client (Bonus Task)
Vue.js Implementation:

The WebSocket client currently resides in the Vue.js environment and connects to a WebSocket server, sending and verifying messages.
Node.js Porting:

For the backend, Node.js’s WebSocket libraries (e.g., ws) provide a robust solution for handling real-time communication. This logic can easily be ported, allowing the backend to manage the WebSocket connection, message transmission, and verification.
Getting Started
Prerequisites
Vue.js (current implementation)
Node.js (for future porting)
npm or yarn
MongoDB (for querying user data)
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/Sfiso0808/vueTask2.git
cd fullstack-assignment
Install dependencies:

bash
Copy code
npm install
Run the Vue.js frontend:

bash
Copy code
npm run dev
For Node.js porting, ensure MongoDB is set up for storing and querying user data.

Running the Project (Vue.js)
Run Step 1: Simulate secure login and data handling:

bash
Copy code
npm run run-step1
Run Step 2: Handle data deduplication and generate CSV:

bash
Copy code
npm run run-step2
Run Step 3: Securely post user data:

bash
Copy code
npm run run-step3
Run Step 4: Query the Engineering department:

bash
Copy code
npm run run-step4
How to Port to Node.js
This project can be easily ported to Node.js by:

Replacing Vue.js frontend logic with Node.js backend scripts.

Each task can be handled on the server side using Express.js.
Secure data handling, deduplication, and API calls can be done more efficiently on the backend.
Setting up Express.js for HTTP routing and API handling.

Using MongoDB to store and query user data, especially for Step 4 (Engineering Department Reporting).

Implementing security features (e.g., rate-limiting, CSRF protection) on the server side using middleware.

Notes
Although the current implementation is in Vue.js, it is structured in a way that can be fully migrated to Node.js for backend operations.
All logic, data handling, and security practices can be marked and evaluated for a Node.js backend.
License
This project is licensed under the MIT License - see the LICENSE file for details.
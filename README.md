Smart Retail Billing Software 🛒

A full-stack billing and retail management system built with Spring Boot, React, and MySQL.
This project is designed to help small and medium-sized businesses manage categories, products, orders, and users through an easy-to-use web interface.

⸻

🚀 Tech Stack

Backend (Java + Spring Boot)
	•	Spring Boot 3 – REST API development
	•	Spring Data JPA (Hibernate) – ORM for database interaction
	•	Spring Security + JWT – Secure authentication
	•	MySQL 9.4 – Relational database
	•	Maven – Dependency management and build tool

Frontend (React + Vite)
	•	React 18 + Vite – Fast single-page app development
	•	React Router – Client-side navigation
	•	Context API / Hooks – State management
	•	Axios / Fetch API – API communication
	•	Custom + Utility CSS – Styling

Other Integrations (Planned)
	•	AWS S3 – File upload support
	•	Razorpay API – Online payment integration

⸻

📂 Project Structure

Smart-Retail-Billing-Software/
│── client/                     # React frontend
│   ├── src/
│   │   ├── components/         # Reusable UI components
│   │   ├── context/            # State management
│   │   ├── pages/              # Application pages (Dashboard, Orders, etc.)
│   │   ├── Service/            # API service layer
│   │   └── util/               # Constants & helpers
│   ├── package.json            # Frontend dependencies
│   └── vite.config.js          # Vite config
│
│── billingsoftware/            # Spring Boot backend
│   ├── src/main/java/          # Application code
│   ├── src/main/resources/
│   │   └── application.properties  # DB + Server config
│   ├── pom.xml                 # Maven dependencies
│   └── mvnw                    # Maven wrapper
│
│── billing_app.sql             # MySQL schema & tables
│── README.md                   # Project documentation



⚙️ Setup & Run

1️⃣ Database (MySQL)
# Login as root
mysql -u root -p

# Create database and user
CREATE DATABASE billing_app CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'billing_user'@'localhost' IDENTIFIED BY 'Deepak04@';
GRANT ALL PRIVILEGES ON billing_app.* TO 'billing_user'@'localhost';
FLUSH PRIVILEGES;

# Import schema
mysql -u billing_user -p billing_app < billing_app.sql

2️⃣ Backend (Spring Boot)
cd billingsoftware
./mvnw -Dmaven.compiler.release=17 spring-boot:run

3️⃣ Frontend (React + Vite)
cd client
npm install
npm run dev



✨ Features
	•	✅ User authentication with JWT
	•	✅ Category & Product management
	•	✅ Order creation & invoice generation
	•	✅ Persistent data storage with Spring Data JPA + MySQL
	•	✅ Fully integrated REST API with React frontend
	•	🔜 File uploads via AWS S3
	•	🔜 Online payments via Razorpay



📖 API Endpoints
Method   | Endpoint         | Description
---------|------------------|---------------------
POST     | /auth/login      | Login & get JWT
GET      | /categories      | List categories
POST     | /categories      | Create category
GET      | /items           | List items
POST     | /orders          | Create new order
GET      | /orders/{id}     | Get order details


👨‍💻 Author

Deepak Singh
📧 deepaksingh74884@gmail.com
🔗 GitHub Profile
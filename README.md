# 🍫 Sugar Corner — Artisan Brownie Shop Management System

A full-stack web application for managing an artisan brownie shop, built as a university IS project.
Customers can browse products, place orders, and track deliveries. Admins get a complete dashboard
to manage products, orders, payments, and customer relationships.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java 17, Spring Boot 3.2.5 |
| Frontend | Thymeleaf, HTML5, CSS3, Vanilla JS |
| Database | MySQL 8 |
| Build Tool | Maven |
| Server | Embedded Tomcat (Spring Boot) |

---

## ✨ Features

### 👤 Customer Portal
- Register, login, and manage profile
- Browse brownie products with search, category filter, and price filter
- Add to cart with real-time stock enforcement
- Place orders (delivery or pickup) with address details
- View order history and track order status
- Payment history with receipt view
- Contact & feedback system with live chat support
- Loyalty membership tier — New → Regular → Loyal → VIP
- Automatic loyalty discount applied at checkout

### 🛡️ Admin Dashboard
- Secure admin login with session management
- **Customer Management** — view all customers, block/unblock accounts, loyalty tier badges
- **Product Management** — add, edit, hide, delete products with image upload; auto-detect popular products by order frequency
- **Order Management** — view and update order status, admin notes, search by ID or date
- **Payment Management** — mark COD payments as received, process refunds, search and filter payments
- **Contact & Feedback** — live chat with customers, view and manage feedback and ratings
- Real-time notification bell for new orders (persists across login/logout)

---

## 🏗️ Project Structure

```
src/
├── main/
│   ├── java/com/brownieshop/
│   │   ├── config/          # SecurityConfig, WebMvcConfig, UploadConfig
│   │   ├── controller/      # All MVC controllers (Admin + Customer)
│   │   ├── dao/             # JDBC data access objects
│   │   ├── model/           # Domain models (Customer, Product, Order, Payment…)
│   │   └── service/         # Business logic layer
│   └── resources/
│       ├── static/
│       │   ├── videos/      # Background video (bg-video.mp4)
│       │   └── uploads/     # Product images
│       └── templates/
│           ├── admin/       # Admin panel pages
│           ├── contact/     # Contact & feedback pages
│           ├── customer/    # Customer dashboard & profile
│           ├── orders/      # Cart, checkout, order history
│           ├── payments/    # Payment pages
│           └── products/    # Product listing & detail
```

---

## 🚀 Getting Started

### Prerequisites
- Java 17+
- MySQL 8+
- Maven 3.6+

### 1 — Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/sugar-corner.git
cd sugar-corner
```

### 2 — Create the database
```sql
CREATE DATABASE sugarcorner_db;
USE sugarcorner_db;
```
Then run the SQL schema file to create all tables and seed data.

### 3 — Configure database credentials
Edit `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/sugarcorner_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```

### 4 — Add the background video (optional)
Place your video file at:
```
src/main/resources/static/videos/bg-video.mp4
```

### 5 — Run the application
```bash
mvn spring-boot:run
```


---

## 🔑 Default Credentials

| Role | Email | Password |
|---|---|---|
| Admin | admin@sugarcorner.lk | admin123 |
| Customer | kasun@example.com | password123 |

---

## 💎 Loyalty Tier System

| Orders Placed | Tier | Discount |
|---|---|---|
| 0 – 2 | 🌱 New Customer | 0% |
| 3 – 5 | ⭐ Regular Customer | 5% |
| 6 – 10 | 💎 Loyal Customer | 8% |
| 11+ | 👑 VIP Customer | 10% |

Discounts are applied automatically at checkout based on the customer's completed order count.

---

## 📱 Social Media

| Platform | Link |
|---|---|
| Facebook | [Sugar Corner Facebook](https://www.facebook.com/share/15f8FQiHcz/) |
| Instagram | [Sugar Corner Instagram](https://tr.ee/-6CBrcau-M) |
| TikTok | [Sugar Corner TikTok](https://tr.ee/1sfpiJhMAt) |
| WhatsApp | [Chat with us](https://tr.ee/3QfscnrEo3) |

---

## 📄 License

This project was developed as a university Information Systems assignment.
All brownie images and videos are used for educational purposes only.

---

> Made with 🍫 in Sri Lanka

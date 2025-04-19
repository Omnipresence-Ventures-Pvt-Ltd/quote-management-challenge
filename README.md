# 💼 Omnipresence – Saved Quotes Backend Challenge

Welcome to the take-home challenge for the **Senior Backend Engineer** role at [Omnipresence](https://omnipresence.vercel.app) – a fast-scaling B2B eCommerce platform.

This challenge simulates a real-world feature module you’d build on our platform. It tests how you think, code, and ship.
---

✅ Submission Instructions
Fork this repo

Complete the challenge within 48 hours

Push your code to your fork

Share your forked repo link with us via email at: rishitsaraf24@gmail.com

Bonus points for:

Notion/Loom video walking through your code

CI/CD, docker setup, observability practices

---

## 🎯 Objective

Design and implement a **Saved Quotes** module for authenticated buyers.

This includes:
- Creating, modifying, and listing saved quotes
- Automatic expiry handling (14 days)
- Change tracking (audit trail)
- Versioning and rollback
- Optimistic locking

---

## 🧪 What to Build

### Core APIs

| Method | Endpoint         | Description                            |
|--------|------------------|----------------------------------------|
| POST   | `/quotes`        | Save a new quote                       |
| GET    | `/quotes/:id`    | View a saved quote                     |
| PUT    | `/quotes/:id`    | Update a quote (if not expired)        |
| DELETE | `/quotes/:id`    | Soft delete a quote                    |
| GET    | `/quotes`        | List all quotes for the logged-in user |

---

### 🧠 Business Rules

- Quotes expire **14 days** after creation (unless extended)
- Prevent duplicate quotes for the same product+quantity combo within **2 hours**
- All quotes must be **versioned** (e.g., v1, v2, ...)
- Support **optimistic locking** (handle update conflicts gracefully)
- Track **full change history** in a `quote_history` table
- Auth should use **JWT**
- Code must have **schema validation**, error handling, and be modular

---

## ⚙️ Stack

You can use any backend stack, but we recommend:

- **Node.js + Express**
- **PostgreSQL**
- **JWT for auth**
- Any ORM/Query builder (e.g., Prisma, Knex, Sequelize)

---

## 🧪 Testing

- Unit tests for key logic (expiry, locking, etc.)
- 1 integration test (end-to-end flow)
- Use any testing framework (e.g., Jest, Mocha)



<div align="center">

#  Aurora Gallery

**A server-side rendered fine art e-commerce platform with a glassmorphism UI, built on Node.js, Express, and EJS.**

![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-B4CA65?logo=ejs&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)


</div>

---

## Overview

**Aurora Gallery** is a full-stack e-commerce demo for a fine art gallery. Pages are rendered on the server with EJS, and the code follows a clean **MVC architecture** with dynamic routing, a session-backed shopping cart, and a custom frosted-glass UI written in plain CSS with no frameworks.

**What this project demonstrates**
- Structuring a Node.js/Express app with separated models, controllers, and routes
- Server-side rendering with reusable EJS partials
- Server-managed state with `express-session`
- Building a polished, responsive UI without a CSS framework
- Containerizing a Node app with Docker

## ✨ Features

- 🎨 **Gallery browsing:** grid view of artworks with dynamic detail pages (`/shop/:id`)
- 🛒 **Session-based cart:** add and manage items, persisted per user session
- 🧱 **MVC architecture:** clear separation of data, logic, and presentation
- 🧩 **Reusable EJS partials:** shared layout components across pages
- 💎 **Glassmorphism design:** gradients, blur, and frosted cards in vanilla CSS
- 📬 **Contact form:** demo submission flow
- 🐳 **Docker-ready:** includes a `Dockerfile` and `.dockerignore`

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js |
| Framework | Express |
| Templating | EJS (server-side rendering) |
| State | express-session |
| Styling | Vanilla CSS (glassmorphism) |
| Tooling | nodemon, Docker |

## 🏗️ Architecture

```
Request ─► routes/ ─► controllers/ ─► models/ ─► data
                           │
                           └─► views/ (EJS) ─► rendered HTML ─► Client
```

```
SellArt/
├── server.js          # App entry: Express config, sessions, static middleware
├── routes/            # Feature-grouped Express routers
├── controllers/       # Route handlers for pages, products, cart
├── models/            # Domain data and accessors (e.g. artworkModel.js)
├── views/             # EJS templates (pages + partials)
├── public/            # Static assets (CSS, images)
└── Dockerfile
```

## 🗺️ Routes

| Route | Description |
|---|---|
| `/` | Home with featured artworks |
| `/shop` | Gallery grid |
| `/shop/:id` | Artwork detail page |
| `/cart` | Session-backed cart |
| `/about` | Studio story and philosophy |
| `/contact` | Contact form (demo) |

## 📸 Screenshots

| Home | Shop | Product | Cart |
|---|---|---|---|
| ![](docs/screenshots/home.png) | ![](docs/screenshots/shop.png) | ![](docs/screenshots/product.png) | ![](docs/screenshots/cart.png) |

## 🚀 Getting Started

**Prerequisites:** Node.js 18+ and npm

```bash
# 1. Clone
git clone https://github.com/vinayarpillai2027/SellArt.git
cd SellArt

# 2. Install dependencies
npm install

# 3. Run
npm start          # production
npm run dev        # development with auto-reload (nodemon)
```

Open **http://localhost:3000**

### 🐳 Run with Docker

```bash
docker build -t sellart .
docker run -p 3000:3000 sellart
```

## 🔮 Roadmap

- [ ] Persistent database (MongoDB/PostgreSQL) in place of in-memory data
- [ ] User authentication and order history
- [ ] Payment integration (Stripe/Razorpay)
- [ ] Admin panel for managing artworks
- [ ] Automated tests and CI with GitHub Actions

## 👤 Author

**Vinaya R Pillai**
[GitHub](https://github.com/vinayarpillai2027) · [LinkedIn](#) · [Email](#)

---
⭐ If you found this useful, consider starring the repo!

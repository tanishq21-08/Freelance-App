# Full-Stack Freelance Marketplace with AI

A Fiverr-inspired freelance marketplace built with React, Node.js, Express, and MongoDB — featuring AI-powered gig descriptions, sentiment analysis on reviews, Stripe payments, and real-time chat.

## Features

- **Freelance Marketplace** — Buyers browse gigs, place orders, leave reviews. Sellers create gigs, manage orders, track earnings
- **Stripe Payment Integration** — Secure checkout flow with order creation, payment processing, and confirmation
- **Real-Time Chat** — Bidirectional messaging between buyers and sellers
- **AI Gig Description Generator** — Sellers enter keywords and the AI generates professional, optimized gig listings using OpenAI GPT API
- **AI Review Analyzer** — Detects sentiment and highlights key phrases in buyer reviews, giving sellers actionable insights
- **Image Uploads** — Cloudinary integration for gig images and user avatars
- **Advanced Search & Filtering** — Filter gigs by category, price range, delivery time, and search queries

## Tech Stack

**Frontend:** React, React Router DOM, React Query, SCSS, Stripe.js

**Backend:** Node.js, Express.js, MongoDB, Mongoose

**Auth:** JWT, Cookie-based authentication, Express middleware, error handling

**Payments:** Stripe payment gateway

**AI:** OpenAI GPT API (gig descriptions, review sentiment analysis)

**Other:** Cloudinary (image uploads), React Query (data fetching + mutations)

## Project Structure

```
├── client/                  # React frontend
│   ├── src/
│   │   ├── components/      # Navbar, Footer, GigCard, Reviews, ChatWindow
│   │   ├── pages/           # Home, Gigs, SingleGig, Orders, Messages, Add, Login, Register
│   │   └── utils/           # API config, helpers, reducers
│   └── public/              # Static assets
├── api/                     # Express backend
│   ├── controllers/         # Auth, Gig, Order, Review, Chat, Message controllers
│   ├── routes/              # REST API route definitions
│   ├── models/              # MongoDB/Mongoose schemas (User, Gig, Order, Review, Chat, Message)
│   └── middleware/          # JWT verification, error handler
```

## Setup

**Prerequisites:** Node.js, MongoDB, Cloudinary account, Stripe account, OpenAI API key

**Backend:**
```bash
cd api
npm install
# Create .env with MONGO_URI, JWT_SECRET, STRIPE_SECRET_KEY, OPENAI_API_KEY
node server.js
```

**Frontend:**
```bash
cd client
npm install
npm run dev
```

## Key Implementations

- **JWT + Cookie Auth** — Secure login/register with httpOnly cookies, middleware-protected routes
- **Stripe Checkout** — Complete payment flow from order creation to payment confirmation
- **React Query** — Efficient data fetching with caching, mutations for create/update operations
- **MongoDB Filtering** — Query-based gig filtering using `req.query` for dynamic search
- **useReducer** — Complex form state management for gig creation with multiple fields
- **Cloudinary Uploads** — Client-side image upload widget with optimized delivery

# AI Agents Website

A showcase platform for custom AI agents and tools, allowing users to explore, test, and subscribe to advanced AI-powered services.

## Table of Contents

* [Features](#features)
* [Tech Stack](#tech-stack)
* [Prerequisites](#prerequisites)
* [Installation](#installation)
* [Running Locally](#running-locally)
* [Deployment](#deployment)
* [Environment Variables](#environment-variables)
* [Directory Structure](#directory-structure)
* [Contributing](#contributing)
* [License](#license)

## Features

* **Agent Gallery**: Browse and interact with a library of AI agents.
* **Subscription Plans**: Stripe-powered subscription management.
* **User Authentication**: Secure sign up, login, and profile management (JWT).
* **Agent Dashboard**: Personalized dashboard to manage active subscriptions and agent usage.
* **Responsive Design**: Mobile-first UI built with Next.js and Tailwind CSS.

## Tech Stack

* **Frontend**: Next.js, React, Tailwind CSS
* **Backend**: Node.js, Express.js (or FastAPI)
* **Database**: PostgreSQL (managed via Sequelize or Prisma)
* **Authentication**: JSON Web Tokens (JWT)
* **Payments**: Stripe
* **Deployment**: Vercel (frontend), DigitalOcean App Platform or Fly.io (backend)

## Prerequisites

* Node.js (v16+)
* npm or yarn
* Git
* A PostgreSQL database (local or cloud)
* A Stripe account (for subscription handling)

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/YOUR_GITHUB_USERNAME/ai-agents-website.git
   cd ai-agents-website
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   Copy the `.env.example` to `.env.local` and fill in your credentials:

   ```bash
   cp .env.example .env.local
   ```

## Running Locally

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Deployment

1. **Push your code to GitHub**:

   ```bash
   git add .
   git commit -m "chore: setup project"
   git push origin main
   ```

2. **Connect to Vercel**:

   * Import the GitHub repo into Vercel.
   * Configure build settings:

     * Framework Preset: Next.js
     * Build Command: `npm run build`
     * Output Directory: `.next`

3. **Set Environment Variables** in Vercel dashboard (Production and Preview):

   * `NEXT_PUBLIC_API_URL`
   * `STRIPE_PUBLIC_KEY`
   * `STRIPE_SECRET_KEY`
   * `JWT_SECRET`
   * `DATABASE_URL`

4. **Add Custom Domain**:

   * `decentrlaai.com` and `www.decentrlaai.com`
   * Update Namecheap DNS records (A/CNAME) as described in documentation.

## Environment Variables

```env
# Frontend
NEXT_PUBLIC_API_URL=https://api.yourdomain.com

# Stripe
STRIPE_PUBLIC_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...

# Auth
JWT_SECRET=your_jwt_secret

# Database
DATABASE_URL=postgres://user:password@host:port/dbname
```

## Directory Structure

```
├── components/       # Reusable React components
├── pages/            # Next.js pages (routes)
├── public/           # Static assets
├── styles/           # Global styles / Tailwind config
├── api/              # Backend API routes (Express or FastAPI)
├── models/           # Database models (Sequelize/Prisma)
├── utils/            # Utility functions and hooks
└── README.md         # Project documentation
```

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "feat: add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

Please follow the [Code of Conduct](CODE_OF_CONDUCT.md) and the [Contributor Guidelines](CONTRIBUTING.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

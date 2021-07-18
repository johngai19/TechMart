# TechMart: E-commerce Platform

Welcome to the TechMart E-commerce Platform repository. This repository contains the source code for a full-stack e-commerce application built with modern web technologies. The project is designed to provide a robust and scalable solution for online retail businesses.

## Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Screenshots](#screenshots)
- [Installation and Setup](#installation-and-setup)
- [Backend Configuration](#backend-configuration)
- [Frontend Configuration](#frontend-configuration)
- [Contributing](#contributing)
- [License](#license)

## Overview

TechMart is a comprehensive e-commerce platform built with Next.js, TypeScript, and Prisma. The application offers a seamless shopping experience with features like user authentication, product listing, cart management, and secure checkout using Stripe.

## Technologies Used

### Frontend

- **Next.js** - A React framework for server-side rendering and static site generation.
- **TypeScript** - A statically typed superset of JavaScript.
- **Tailwind CSS** - A utility-first CSS framework for rapid UI development.
- **React Query** - A library for fetching, caching, and updating data in React applications.
- **NextAuth** - A library for authentication in Next.js applications.
- **Yup** - A JavaScript schema builder for value parsing and validation.

### Backend

- **Node.js** - A JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Prisma** - An ORM for Node.js and TypeScript.
- **PostgreSQL** - A powerful, open-source object-relational database system.
- **Stripe** - A suite of APIs for handling online payments.

### Others

- **Docker** - A tool designed to make it easier to create, deploy, and run applications by using containers.
- **Sentry** - An error tracking and performance monitoring tool.

## Features

- **User Authentication**: Sign in with GitHub using NextAuth.
- **Product Management**: View and manage products listed on the platform.
- **Cart Management**: Add products to the cart and manage the cart items.
- **Checkout Process**: Secure checkout using Stripe integration.
- **Error Tracking**: Integrated with Sentry for error tracking and monitoring.

## Installation and Setup

### Prerequisites

- Node.js (v14.x or higher)
- Docker
- PostgreSQL

### Clone the Repository

```bash
git clone https://github.com/johngai19/TechMart.git
cd TechMart
```

### Configure Environment Variables

Create a `.env` file in the root directory and fill in the necessary environment variables:

```env
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_DB=
DATABASE_URL="postgresql://<POSTGRES_USER>:<POSTGRES_PASSWORD>@<POSTGRES_HOST>:<POSTGRES_PORT>/<POSTGRES_DB>?schema=public&sslmode=prefer"
GITHUB_SECRET=
GITHUB_ID=
SECRET=
NEXTAUTH_URL=
NEXTAUTH_CALLBACK_URL=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_SECRET_KEY=
NEXT_PUBLIC_STRIPE_SUCCESS_REDIRECT_URL=
NEXT_PUBLIC_STRIPE_ERROR_REDIRECT_URL=
```

### Install Dependencies

```bash
npm install
```

### Generate Prisma Client

```bash
npx prisma generate
```

### Run Docker Compose

```bash
docker-compose up -d
```

### Run the Development Server

```bash
npm run dev
```

## Backend Configuration

The backend is built with Node.js and Prisma ORM. It uses PostgreSQL as the database. The main configuration file for Prisma is `prisma/schema.prisma` which defines the data models and relationships.

### Prisma Schema

The Prisma schema defines the following models:

- **User**: Represents a user in the system.
- **Product**: Represents a product available for purchase.
- **Account**: Represents a user account linked to an authentication provider.
- **Session**: Represents a user session.
- **VerificationToken**: Represents a verification token for email verification.

### API Endpoints

- **User Authentication**: `/api/auth/[...nextauth]`
- **Product Management**: `/api/products`
- **Checkout Process**: `/api/checkout/products`

## Frontend Configuration

The frontend is built with Next.js and TypeScript. It uses Tailwind CSS for styling and React Query for data fetching and state management.

### Components

- **Layout**: The main layout component that wraps all pages.
- **Header**: The header component containing the navigation bar.
- **Product**: The product component that displays product details.
- **Cart**: The cart component that manages cart items and checkout process.

### Pages

- **Home**: The homepage that displays the list of products.
- **SignIn**: The sign-in page for user authentication.
- **Error**: Custom error pages for handling errors.

## Contributing

We welcome contributions from the community. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request. Please adhere to our [Code of Conduct](CODE_OF_CONDUCT.md).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
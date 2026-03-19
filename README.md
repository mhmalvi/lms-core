# LMS Core

A generic, extensible Learning Management System platform built with **Laravel 8** and **Vue 3**, designed as a foundational codebase for deploying customized LMS instances.

## Overview

LMS Core provides the essential backend API and frontend SPA architecture for a modern learning management system. Built with a clean separation between the Laravel API backend and Vue.js single-page application frontend, it serves as the core platform that can be extended and branded for specific institutional deployments.

## Tech Stack

| Layer       | Technology                                       |
|-------------|--------------------------------------------------|
| Backend     | PHP 7.3+ / 8.0, Laravel 8                       |
| Frontend    | Vue 3, Vue Router 4, Vuex 4                     |
| Auth        | Laravel Sanctum                                  |
| Database    | MySQL                                            |
| Build Tools | Laravel Mix 6, Webpack                           |
| Testing     | PHPUnit, Mockery                                 |

## Key Features

### API-First Architecture
- RESTful API backend with Laravel Sanctum authentication
- Clean separation of concerns between backend and frontend
- Token-based API authentication for SPA consumption

### Vue 3 SPA Frontend
- Modern single-page application built with Vue 3
- Client-side routing via Vue Router 4
- Centralized state management with Vuex 4
- Pagination support with v-pagination-3

### Core Platform
- User authentication and management
- Extensible model and controller architecture
- Database migration framework
- Environment-based configuration

## Project Structure

```
app/
├── Http/Controllers/       # API and web controllers
├── Http/Middleware/         # Request middleware
├── Models/                 # Eloquent models
└── Providers/              # Service providers
resources/js/
├── app.js                  # Vue 3 app entry point
└── bootstrap.js            # Axios and dependency setup
routes/
├── api.php                 # API routes
└── web.php                 # Web routes
```

## Prerequisites

- PHP >= 7.3
- Composer
- Node.js & npm
- MySQL

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/mhmalvi/lms-core.git
   cd lms-core
   ```

2. **Install dependencies**
   ```bash
   composer install
   npm install
   ```

3. **Configure environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Set up the database**

   Configure your MySQL connection in `.env` and run:
   ```bash
   php artisan migrate
   ```

5. **Build frontend assets**
   ```bash
   npm run dev        # Development
   npm run production # Production
   ```

6. **Start the server**
   ```bash
   php artisan serve
   ```

## Extending the Platform

LMS Core is designed to be forked and extended for specific institutional needs. Key extension points include:

- **Models** — Add domain-specific models in `app/Models/`
- **API Controllers** — Extend the API layer in `app/Http/Controllers/`
- **Vue Components** — Build feature-specific UI in `resources/js/components/`
- **Routes** — Define new API and web routes in `routes/`

## License

This project is proprietary software.
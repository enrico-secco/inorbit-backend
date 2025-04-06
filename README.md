<div align="center">
    <img src="public/logo.png" alt="Inorbit Backend Logo">
</div>

# Inorbit Backend

This project is the backend for a simple weekly habit tracker. It provides APIs to manage goals, track completions, and retrieve weekly summaries of progress.

## Features

- Create and manage goals with desired weekly frequencies.
- Track goal completions.
- Retrieve pending goals for the week.
- Get a summary of weekly progress.

## Technologies and Libraries Used

#### Backend Framework
- **[Fastify](https://www.fastify.io/):** A fast and low-overhead web framework for Node.js.

#### Database
- **[PostgreSQL](https://www.postgresql.org/):** A powerful, open-source relational database.
- **[Drizzle ORM](https://orm.drizzle.team/):** A type-safe ORM for interacting with the database.

#### Validation and Type Safety
- **[Zod](https://zod.dev/):** A TypeScript-first schema declaration and validation library.
- **[fastify-type-provider-zod](https://github.com/fastify/fastify-type-provider-zod):** Integration of Zod with Fastify for type-safe validation.

#### Utilities
- **[Day.js](https://day.js.org/):** A lightweight JavaScript library for date manipulation.
- **[CUID2](https://github.com/paralleldrive/cuid2):** A collision-resistant ID generator.

#### Environment Configuration
- **[dotenv](https://github.com/motdotla/dotenv):** For managing environment variables (via `.env`).

#### Development Tools
- **[TypeScript](https://www.typescriptlang.org/):** A strongly typed programming language that builds on JavaScript.
- **[TSX](https://github.com/esbuild-kit/tsx):** A fast TypeScript execution environment.
- **[Biome](https://biomejs.dev/):** A tool for formatting, linting, and organizing imports.

#### Containerization
- **[Docker](https://www.docker.com/):** Used for running PostgreSQL in a containerized environment.

#### Migrations
- **[Drizzle Kit](https://github.com/drizzle-team/drizzle-kit):** A migration tool for Drizzle ORM.

## Getting Started

### Prerequisites
- Node.js (v16 or later)
- A PostgreSQL database (e.g., NeonDB or a local instance via Docker)

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd inorbit-backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the environment variables: Create a .env file in the root directory and add the following:
   ```bash
   DATABASE_URL=postgres://<username>:<password>@<host>:<port>/<database>
   ```

4. (Optional) If running the database locally, start PostgreSQL using Docker:
   ```bash
   docker-compose up -d
   ```

5. Seed the database:
   ```bash
   npm run seed
   ```

6. Start the development server:
   ```bash
   npm run dev
   ```

## API Endpoints
- POST /goals: Create a new goal.
- POST /completions: Track a goal completion.
- GET /pending-goals: Retrieve pending goals for the week.
- GET /summary: Get a weekly summary of progress.
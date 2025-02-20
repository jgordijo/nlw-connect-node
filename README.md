# NLW Connect

## Project Description
- The project consists of subscribing to a fictional event and being able to refer friends to do the same.
- Once subscribed, the user receives a URL that can be shared.
- Clicks and referred users are tracked and displayed in a rank.

## Requirements

- Node.js v22.13.1
- Docker
- `.env` file (`.env.example` is provided)

## How to run the project

- Install Node.js LTS
- Clone the project
- Install project dependencies running `npm install`
- Run `docker compose up -d`
- Run `npx drizzle-kit migrate` to run the existing migrations and create the datbabase structure.
- Start the service running `npm run dev`. The service will run on port 3333 by default.

## API Docs
- Docs can be found at http://localhost:3333/docs

## File Tree Structure

```bash
└── 📁nlw-connect-node
    └── 📁.vscode
        └── settings.json # VSCode settings for this repo
    └── 📁src # Source Code Directory
        └── 📁drizzle # Drizzle ORM related
            └── client.ts
            └── 📁migrations
            └── 📁schema
                └── subscriptions.ts
        └── 📁functions # Use cases
            └── access-invite-link.ts
            └── get-ranking.ts
            └── get-subscriber-invite-clicks.ts
            └── get-subscriber-invites-count.ts
            └── get-subscriber-ranking-position.ts
            └── subscribe-to-event.ts
        └── 📁redis # Redis
            └── client.ts
        └── 📁routes # Routes
            └── access-invite-link-route.ts
            └── get-ranking-route.ts
            └── get-subscriber-invite-clicks-route.ts
            └── get-subscriber-invites-count-route.ts
            └── get-subscriber-ranking-position-route.ts
            └── subscribe-to-event-route.ts
        └── server.ts
    └── .env.example # Environment Variables example
    └── .gitignore # Files/Folders to be ignored by git
    └── .nvmrc # Node version
    └── biome.json # Biome JS Linter configuration
    └── docker-compose.yml # Docker compose file
    └── drizzle.config.ts # Drizzle ORM configuration file
    └── package-lock.json # Locked versions of all dependencies
    └── package.json # Project metadata and dependencies
    └── README.md #Project overview
    └── tsconfig.json # TypeScript configuration
    └── tsup.config.ts # TS Up config, for deploy
```

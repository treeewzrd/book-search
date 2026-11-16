# Book Search

![Status](https://img.shields.io/badge/status-coursework-blue)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

Coursework application for searching Google Books and saving books to a signed-in account.

**Built with:** React, TypeScript, GraphQL, Apollo, Express, MongoDB.

## What I built

- Built a Google Books search interface and saved-book views using React and TypeScript.
- Implemented GraphQL queries and mutations for account registration, login, and each user's saved books.
- Connected MongoDB models with bcrypt password hashing and JWT authentication.

## Explore the source

- [client/src/pages/SearchBooks.tsx](client/src/pages/SearchBooks.tsx) — Search interface and Google Books requests.
- [server/src/schemas/resolvers.ts](server/src/schemas/resolvers.ts) — Account and saved-book operations.
- [server/src/models/User.ts](server/src/models/User.ts) — User schema and password hashing.

## Run locally

Requires Node.js/npm and MongoDB. From the repository root:

```bash
npm install
```

Create a private `server/.env` with:

```dotenv
MONGODB_URI=mongodb://127.0.0.1:27017/googlebooks
JWT_SECRET_KEY=replace_with_a_long_random_secret
```

Build before starting development: the backend watcher runs compiled files.

```bash
npm run build
npm run develop
```

Open the frontend address printed in the terminal. After backend source changes, rebuild the server using `npm run build --prefix server`.

No working automated test suite is configured in the server package.

Setup instructions were checked against source; builds and application behavior have not been rerun during this cleanup.

**License:** [MIT](LICENSE).

# Solar ERP

Solar ERP lead and operations workspace.

## Run locally

1. Install dependencies with `npm install` or `bun install`.
2. Copy `.env.example` to `.env` and configure the environment values.
3. Start the development server with `npm run dev`.
4. Build the application with `npm run build`.

## Performance refactor

- Workspace screens and large modals load on demand, reducing the JavaScript required for the first screen.
- Dashboard follow-ups reuse the dashboard response already loaded by the app.
- Lead table search filtering is memoized.
- Database indexes support lead sorting/scoping and common follow-up queries.

The refactor preserves existing authorization checks, filters, calculations, and workflow transitions.

The source repository's `data/` directory is not included in this archive because it contains PostgreSQL database files. The app initializes its database from `server/db/schema.sql` and seed routines.

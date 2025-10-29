Example of slowness in Medusa with a product that has 500 variants.

To get this up and running:
- Clone the repo
- Set up a database locally with docker
  - `docker run --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=medusa -d postgres:16.3`
  - `npx medusa db:setup --db medusa`
- Set database url in .env file
  - `postgres://postgres:postgres@localhost/medusa`
- Seed database using /src/scripts/seed.ts
  - `npx medusa exec ./src/scripts/seed.ts`
- Create a user
  - `npx medusa user --email admin@medusa.local --password supersecret`

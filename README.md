# WebBase - Next.js 15 Starter

Modern Next.js 15 template with:

- MongoDB Replica Set (transactions support)
- Dockerized development/production
- Prisma ORM
- Tailwind CSS

## 🚀 Quick Start

### Prerequisites

- Node.js 20+
- Docker & Docker Compose
- MongoDB Compass (optional)

```bash
# Clone and install
git clone https://github.com/ebtkar-altqni/webbase.git
cd webbase
npm install

```

---

## 🛠️ Development Commands

| Command         | Description                                       |
| --------------- | ------------------------------------------------- |
| `npm run dev`   | Starts Next.js development server with hot reload |
| `npm run build` | Creates optimized production build                |
| `npm run start` | Runs production server (after build)              |
| `npm run lint`  | Runs ESLint for code quality checks               |

---

## 🐳 Docker Operations

### Development

| Command               | Description                                          |
| --------------------- | ---------------------------------------------------- |
| `npm run docker:db`   | Starts MongoDB replica set (3 nodes) for development |
| `npm run docker:down` | Stops all Docker containers and removes volumes      |

### Production

| Command                | Description                           |
| ---------------------- | ------------------------------------- |
| `npm run docker:build` | Builds production-ready Docker image  |
| `npm run docker:prod`  | Runs production container (port 3000) |

---

## 📦 Database Management (Prisma)

| Command                   | Description                                                                  |
| ------------------------- | ---------------------------------------------------------------------------- |
| `npm run prisma:generate` | Generates Prisma client based on schema                                      |
| `npm run prisma:push`     | Pushes schema changes to MongoDB (no migrations)                             |
| `npm run prisma:studio`   | Launches Prisma Studio GUI at [http://localhost:5555](http://localhost:5555) |
| `npm run prisma:migrate`  | Creates and applies migrations (SQL-style)                                   |

---

## 🔧 Utility Scripts

| Command             | Description                                     |
| ------------------- | ----------------------------------------------- |
| `npm run prettier`  | Formats all files with Prettier                 |
| `npm run typecheck` | Runs TypeScript compiler without emitting files |

---

## 🏗️ Production Deployment

```bash
# 1. Build and start
docker-compose -f docker-compose.prod.yml up --build -d

# 2. Environment setup
cp .env.example .env
nano .env  # Edit variables as needed
```

---

## 📂 Folder Structure

```
webbase/
├── docker/                 # Docker configs
├── prisma/                 # Database schema
├── src/                    # Next.js app
├── .env.example            # Environment template
├── docker-compose.yml      # Dev environment
└── docker-compose.prod.yml # Production environment
```

---

## 🌐 Access Points

- Next.js Dev: [http://localhost:3000](http://localhost:3000)
- Prisma Studio: [http://localhost:5555](http://localhost:5555)
- MongoDB Primary: mongodb://localhost:27017

---

## 🔄 Typical Workflow

### Start MongoDB:

```bash
npm run docker:db
```

### Develop with hot reload:

```bash
npm run dev
```

### When ready for production:

```bash
npm run docker:build
npm run docker:prod
```

---

### Key Features in This Version:

1. **Command Matrix** - Clear tabular layout showing all npm scripts with descriptions
2. **Lifecycle Separation** - Distinct sections for dev/prod/database operations
3. **Libya-Optimized** -

   - Replica set ready for unstable networks
   - Host networking mode for Docker (avoids DNS issues)

4. **Visual Cues** - Emoji icons for quick scanning
5. **Production Focus** - Includes complete deploy commands

```

```

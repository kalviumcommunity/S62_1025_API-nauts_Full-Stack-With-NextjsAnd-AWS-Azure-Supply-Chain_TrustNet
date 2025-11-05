# TrustNet – Lightweight Digital Identity Verification for Local Businesses

TrustNet empowers small-scale entrepreneurs and local businesses by giving them credible, verified digital identities. Traditional Know-Your-Customer (KYC) processes are too document-heavy for micro-businesses, street vendors, and home-based entrepreneurs. TrustNet solves this by offering community validation, UPI transaction-based trust signals, and analytics that help local entrepreneurs build and showcase their credibility online.

---

## 📁 Folder Structure

```
TrustNet/
│
├── app/
│   ├── page.tsx                 → Home page (frontend UI)
│   ├── dashboard/
│   │   └── page.tsx             → Dashboard view for business insights
│   └── api/
│       ├── users/
│       │   └── route.ts         → API endpoint for user management
│       ├── auth/
│       │   └── route.ts         → OTP-based authentication API
│       └── business/
│           └── route.ts         → Business profile CRUD operations
│
├── components/
│   ├── Navbar.tsx               → Top navigation bar component
│   ├── Footer.tsx               → Footer component
│   ├── BusinessCard.tsx         → Displays business details and trust score
│   └── AnalyticsChart.tsx       → Chart.js component for analytics dashboard
│
├── lib/
│   ├── db.ts                    → Database connection logic (PostgreSQL)
│   ├── auth.ts                  → Authentication and session utilities
│   ├── trustScore.ts            → Core logic for trust score calculation
│   └── redis.ts                 → Redis caching configuration
│
├── public/
│   └── logo.png                 → Project logo for README and UI
│
├── styles/
│   └── globals.css              → Global Tailwind CSS and style settings
│
├── .env.local                   → Environment variables (not committed)
├── next.config.js               → Next.js configuration
├── package.json                 → Dependencies and project metadata
└── README.md                    → Project documentation

```

---

## Setup and Installation

### 1. Prerequisites

- Node.js 20 or higher
- PostgreSQL 15 or higher
- Redis 7 or higher
- Docker (optional but recommended)
- AWS or Azure account for deployment

### 2. Installation

Clone the repository
git clone https://github.com/kalviumcommunityS62_1025_API-nauts_Full-Stack-With-NextjsAnd-AWS-Azure-Supply-Chain_TrustNet.git
cd trustnet

Install dependencies
npm install

Setup environment variables
cp .env.example .env

Add your database URL, Redis URL, and required environment keys
Run Prisma migrations
npx prisma migrate dev

Seed initial data (optional)
npx prisma db seed

### 3. Running Locally

Start the Next.js development server
npm run dev

Visit http://localhost:3000 to view the application.

### 4. Using Docker

Build and run containers
docker-compose up --build

---

## Reflection: Structural Design Rationale

The structure and technologies were chosen to maximize modularity, scalability, and performance across future sprints.

- Next.js 14 provides full-stack capabilities with built-in API routes, ensuring frontend and backend alignment.
- PostgreSQL with Prisma offers a robust ORM layer and easily maintainable schema evolution.
- Redis caching enhances performance for analytics and trust score computations.
- Docker ensures consistent development and production environments.

This structure supports collaborative scaling for future sprint pipelines where each subsystem (analytics, verification, dashboard) can evolve independently with minimal coupling.

---

## Screenshot

Add a screenshot of your local application running below.

Example placeholder:

![TrustNet Dashboard](dashboard.png)

---

## Future Enhancements

- Mobile app integration for field agents and vendors
- Advanced analytics with AI-driven trust prediction
- Multi-language support for vernacular inclusivity
- Integration with government micro-loan identity networks

---

## Contributors

| Role                | Team Member         | Key Responsibilities                                          |
| ------------------- | ------------------- | ------------------------------------------------------------- |
| Frontend Lead       | Claudia Jerome      | Next.js UI components, responsive design, analytics dashboard |
| Backend Lead        | Tejas Philip Thomas | Database design, API routes, UPI verification system          |
| Full-Stack & DevOps | Isaac Reji          | Prisma schema, Redis integration, Docker setup, deployment    |
| Quality Assurance   | All Members         | Testing, bug reporting, user experience validation            |

---

## Code Quality Configuration

### TypeScript

We enabled strict mode to catch potential issues early:

- `"strict": true` ensures all types are defined.
- `"noImplicitAny": true` prevents untyped variables.
- `"noUnusedLocals"` and `"noUnusedParameters"` clean up unused code.

### ESLint + Prettier

Our ESLint configuration extends `next/core-web-vitals` and Prettier rules to ensure clean, readable, and consistent code.
We enforce:

- No console logs in production.
- Mandatory semicolons.
- Double quotes for all strings.

### Husky + lint-staged

We use Husky and lint-staged to automatically lint and format code before commits.  
This ensures that no badly formatted code enters our repository.

### Example Output

When committing code that violates lint rules, Husky blocks the commit until all issues are fixed.

## Development Workflow.

---

### Branch Naming Convention

### Format

{type}/{short-description}

### Types

- `feat/` - New features
- `fix/` - Bug fixes
- `hotfix/` - Critical production fixes
- `docs/` - Documentation updates
- `style/` - Code style changes (formatting, etc.)
- `refactor/` - Code refactoring
- `test/` - Adding tests
- `chore/` - Maintenance tasks

### Examples

- `feat/user-authentication`
- `fix/login-validation`
- `docs/api-endpoints`
- `refactor/auth-system`

### PR TEMPLATE

### Description

<!-- Describe your changes and what problem they solve -->

### Type of Change

- [ ] 🚀 New feature
- [ ] 🐛 Bug fix
- [ ] 📚 Documentation
- [ ] 🎨 Style update
- [ ] ♻️ Code refactor
- [ ] ✅ Test addition
- [ ] 🔧 Chore
- [ ] ⚠️ Breaking change

### Checklist

- [ ] My code follows the project style guidelines
- [ ] I have performed a self-review of my code
- [ ] I have commented my code where necessary
- [ ] I have updated the documentation if needed
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective
- [ ] New and existing unit tests pass locally

### Workflow Reflection

This workflow helps because:

**Code Quality:**

- ESLint/Prettier catch issues early
- Code reviews catch bugs before merging
- Consistent patterns make code maintainable

**Collaboration:**

- Clear PR templates help reviewers understand changes
- Everyone follows same branching conventions
- CI/CD pipeline provides objective quality gates

**Velocity:**

- Automated checks save manual review time
- Clear processes reduce confusion and rework
- Quick feedback loops through CI pipeline

### Screenshots (if applicable)

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)

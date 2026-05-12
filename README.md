apnarooms/
├─ apps/
│  ├─ web/                         # Next.js + React + TypeScript frontend
│  │  ├─ src/
│  │  │  ├─ app/
│  │  │  │  ├─ page.tsx            # Public homepage / listing search
│  │  │  │  ├─ layout.tsx
│  │  │  │  ├─ properties/
│  │  │  │  │  ├─ page.tsx         # All listings
│  │  │  │  │  └─ [id]/
│  │  │  │  │     └─ page.tsx      # Property detail page
│  │  │  │  ├─ checkout/
│  │  │  │  │  └─ [propertyId]/
│  │  │  │  │     └─ page.tsx      # Razorpay checkout screen
│  │  │  │  ├─ dashboard/
│  │  │  │  │  └─ page.tsx         # Tenant dashboard
│  │  │  │  ├─ admin/
│  │  │  │  │  ├─ page.tsx         # Admin overview
│  │  │  │  │  ├─ properties/
│  │  │  │  │  │  ├─ page.tsx
│  │  │  │  │  │  ├─ new/
│  │  │  │  │  │  │  └─ page.tsx
│  │  │  │  │  │  └─ [id]/
│  │  │  │  │  │     └─ edit/
│  │  │  │  │  │        └─ page.tsx
│  │  │  │  │  ├─ bookings/
│  │  │  │  │  │  └─ page.tsx
│  │  │  │  │  ├─ leads/
│  │  │  │  │  │  └─ page.tsx      # Basic CRM pipeline
│  │  │  │  │  ├─ users/
│  │  │  │  │  │  └─ page.tsx
│  │  │  │  │  └─ payments/
│  │  │  │  │     └─ page.tsx
│  │  │  │  ├─ login/
│  │  │  │  │  └─ page.tsx         # Google + phone OTP login
│  │  │  │  └─ globals.css
│  │  │  ├─ components/
│  │  │  │  ├─ layout/
│  │  │  │  ├─ auth/
│  │  │  │  ├─ properties/
│  │  │  │  ├─ checkout/
│  │  │  │  ├─ admin/
│  │  │  │  └─ ui/
│  │  │  ├─ lib/
│  │  │  │  ├─ api.ts              # Backend API client
│  │  │  │  ├─ firebase.ts         # Firebase client SDK
│  │  │  │  ├─ auth.ts             # Client auth helpers
│  │  │  │  ├─ razorpay.ts         # Load Razorpay checkout script
│  │  │  │  └─ storage.ts          # Firebase Storage upload helpers
│  │  │  ├─ hooks/
│  │  │  │  ├─ useAuth.ts
│  │  │  │  └─ useAdminGuard.ts
│  │  │  ├─ types/
│  │  │  └─ middleware.ts          # Optional route protection
│  │  ├─ public/
│  │  ├─ package.json
│  │  ├─ next.config.ts
│  │  └─ tsconfig.json
│  │
│  └─ api/                         # Node.js backend
│     ├─ src/
│     │  ├─ server.ts              # App entry
│     │  ├─ app.ts                 # Express/Fastify setup
│     │  ├─ config/
│     │  │  ├─ env.ts
│     │  │  ├─ firebase-admin.ts   # Firebase Admin SDK
│     │  │  └─ razorpay.ts
│     │  ├─ middleware/
│     │  │  ├─ auth.middleware.ts  # Verify Firebase ID token
│     │  │  ├─ admin.middleware.ts # Role check
│     │  │  ├─ error.middleware.ts
│     │  │  └─ rate-limit.ts
│     │  ├─ modules/
│     │  │  ├─ auth/
│     │  │  │  ├─ auth.routes.ts
│     │  │  │  └─ auth.service.ts
│     │  │  ├─ users/
│     │  │  │  ├─ users.routes.ts
│     │  │  │  ├─ users.service.ts
│     │  │  │  └─ users.validators.ts
│     │  │  ├─ properties/
│     │  │  │  ├─ properties.routes.ts
│     │  │  │  ├─ properties.service.ts
│     │  │  │  └─ properties.validators.ts
│     │  │  ├─ bookings/
│     │  │  │  ├─ bookings.routes.ts
│     │  │  │  └─ bookings.service.ts
│     │  │  ├─ payments/
│     │  │  │  ├─ payments.routes.ts
│     │  │  │  ├─ payments.service.ts
│     │  │  │  ├─ razorpay.service.ts
│     │  │  │  └─ webhook.routes.ts
│     │  │  ├─ leads/
│     │  │  │  ├─ leads.routes.ts
│     │  │  │  └─ leads.service.ts
│     │  │  ├─ coupons/
│     │  │  │  ├─ coupons.routes.ts
│     │  │  │  └─ coupons.service.ts
│     │  │  └─ uploads/
│     │  │     ├─ uploads.routes.ts
│     │  │     └─ uploads.service.ts
│     │  ├─ utils/
│     │  │  ├─ async-handler.ts
│     │  │  ├─ api-error.ts
│     │  │  └─ logger.ts
│     │  └─ types/
│     ├─ package.json
│     └─ tsconfig.json
│
├─ packages/
│  ├─ db/
│  │  ├─ prisma/
│  │  │  ├─ schema.prisma
│  │  │  ├─ migrations/
│  │  │  └─ seed.ts
│  │  ├─ src/
│  │  │  └─ prisma.ts             # Prisma client singleton
│  │  └─ package.json
│  │
│  ├─ shared/
│  │  ├─ src/
│  │  │  ├─ types.ts              # Shared frontend/backend types
│  │  │  ├─ constants.ts
│  │  │  └─ validators.ts         # Optional Zod schemas
│  │  └─ package.json
│
├─ docs/
│  ├─ architecture.md
│  ├─ api-routes.md
│  ├─ database-schema.md
│  └─ payment-flow.md
│
├─ scripts/
│  ├─ dev.ps1
│  ├─ migrate.ps1
│  └─ seed.ps1
│
├─ .env.example
├─ package.json
├─ pnpm-workspace.yaml
├─ turbo.json
├─ README.md
└─ .gitignore

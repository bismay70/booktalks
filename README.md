This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Authentication with Clerk

This project is configured to use [Clerk](https://clerk.com/) for authentication via the Next.js App Router. The setup is already included:

1. Install the Clerk SDK:
   ```bash
   npm install @clerk/nextjs
   ```
2. Add your keys to `.env.local` (never commit real values):
   ```bash
   # .env.local
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=YOUR_PUBLISHABLE_KEY
   CLERK_SECRET_KEY=YOUR_SECRET_KEY
   ```
3. A `proxy.ts` file at the project root exports `clerkMiddleware()` and contains the required matcher.  
4. Your application is wrapped with `<ClerkProvider>` in `app/layout.tsx`, and components such as `<SignInButton>`/`<UserButton>` are used in the navbar.

Follow Clerk's up‑to‑date [quickstart guide](https://clerk.com/docs/nextjs/getting-started/quickstart) if you need more details.

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

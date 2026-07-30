<div align="center">
  <h1>Next Supabase Auth</h1>
  <p>A Next.js + Supabase authentication starter with full auth flow — login, sign-up, password reset, email confirmation, protected routes, and dark/light theme, styled with <strong>shadcn/ui</strong>.</p>
  <p>
    <a href="#features">Features</a> ·
    <a href="#getting-started">Getting Started</a> ·
    <a href="#tech-stack">Tech Stack</a> ·
    <a href="#project-structure">Structure</a>
  </p>
  <br/>
</div>

---

## 🔐 Features

- **Full Auth Flow** — Login, sign-up, forgot password, update password, email confirmation
- **Protected Routes** — Authenticated dashboard with guarded layout
- **Supabase SSR** — Server-side auth with cookie-based sessions (App Router)
- **shadcn/ui** — Polished UI components (buttons, cards, inputs, dropdowns, badges)
- **Dark/Light Theme** — System-aware theme switching via `next-themes`
- **Deploy Ready** — One-click deploy to Vercel with Supabase integration

## 🚀 Getting Started

### 1. Create a Supabase Project

You'll need a Supabase project. Create one at [supabase.com/dashboard](https://supabase.com/dashboard).

### 2. Set Up Environment Variables

```bash
cp .env.example .env.local
```

Update `.env.local` with your Supabase project details:

```env
NEXT_PUBLIC_SUPABASE_URL=your-project-url
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=your-publishable-or-anon-key
```

You can find these in your Supabase project settings → **API**.

### 3. Run the Development Server

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the result.

### 4. Build & Deploy

```bash
npm run build
npm start
```

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fathivaratz%2Fnext-supabase-auth)

## 🛠 Tech Stack

| Tech | Description |
|------|-------------|
| [Next.js](https://nextjs.org/) | React framework with App Router |
| [Supabase](https://supabase.com/) | Auth + Database (SSR) |
| [Tailwind CSS](https://tailwindcss.com/) | Utility-first styling |
| [shadcn/ui](https://ui.shadcn.com/) | Accessible UI components |
| [next-themes](https://github.com/pacocoursey/next-themes) | Dark/light mode |
| [TypeScript](https://www.typescriptlang.org/) | Type safety |

## 📁 Project Structure

```
├── app/
│   ├── auth/
│   │   ├── confirm/route.ts        # Email confirmation handler
│   │   ├── error/                  # Auth error page
│   │   ├── forgot-password/        # Password reset form
│   │   ├── login/                  # Login page
│   │   ├── sign-up/                # Sign-up page
│   │   ├── sign-up-success/        # Post-sign-up confirmation
│   │   └── update-password/        # Password update form
│   ├── protected/                  # Authenticated dashboard
│   │   ├── layout.tsx              # Auth guard layout
│   │   └── page.tsx                # Protected content
│   ├── globals.css
│   ├── layout.tsx                  # Root layout with theme provider
│   └── page.tsx                    # Landing page
├── components/
│   ├── ui/                         # shadcn/ui components
│   ├── auth-button.tsx             # Auth status button
│   ├── deploy-button.tsx           # Vercel deploy button
│   ├── forgot-password-form.tsx
│   ├── login-form.tsx
│   ├── sign-up-form.tsx
│   ├── update-password-form.tsx
│   ├── theme-switcher.tsx          # Dark/light toggle
│   └── tutorial/                   # Supabase setup guide components
├── lib/
│   └── supabase/
│       ├── client.ts               # Browser client
│       ├── server.ts               # Server client
│       └── proxy.ts                # Auth proxy
├── proxy.ts                        # Supabase proxy route
├── components.json                 # shadcn/ui config
├── next.config.ts
└── tailwind.config.ts
```

## 📄 License

MIT
# Hireon – Your AI-Powered Career Assistant

Hireon is a full-stack AI-based platform that helps job seekers build ATS-optimized resumes, generate tailored cover letters, and simulate role-specific mock interviews. Powered by Google’s Gemini API and built using the latest web technologies, Hireon is your intelligent companion to navigate the modern job market.

---

## Features

- ✨ **Resume Builder**: Generate ATS-compliant resumes based on your background and target job.
- 📄 **Cover Letter Generator**: Auto-generate personalized letters from job descriptions.
- 🎤 **Mock Interviews**: Get role-specific questions with AI-powered feedback and scoring.
- 📊 **Performance Dashboard**: Visualize your interview performance and track improvements.
- 📬 **Weekly Industry Insights**: Background job updates with top skills and salary trends.
- 📝 **Markdown Editor + PDF Export**: Clean editor for resumes and letters with export support.

---

## Tech Stack

| Layer       | Technology                                  |
|-------------|---------------------------------------------|
| Frontend    | Next.js 15, React 19, Tailwind CSS, Shadcn UI |
| Backend     | Prisma ORM, Neon (PostgreSQL), Inngest      |
| Authentication | Clerk                                     |
| AI Integration | Google's Gemini API            |
| Charts & UI | Recharts, MDX Editor                        |

---

## Architecture Overview

```plaintext
            ┌────────────┐
            │   Client   │
            │ Next.js UI │
            └────┬───────┘
                 │
       ┌─────────▼─────────┐
       │ API Routes (REST) │
       └─────────┬─────────┘
                 │
        ┌────────▼─────────┐
        │  Prisma + Neon   │
        │ (PostgreSQL ORM) │
        └────────┬─────────┘
                 │
      ┌──────────▼───────────┐
      │  Google Gemini API   │
      └──────────────────────┘

- Async background updates via Inngest (e.g., weekly market data)
- Auth protected routes using Clerk
- Resume/letter content stored in markdown format for flexibility
```

## 🚀 Getting Started

Follow these steps to run the project locally:

---

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/hireon.git
cd hireon
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

```bash
DATABASE_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

GEMINI_API_KEY=
```

### 4. Run the Development Server

```bash
npm run dev
```





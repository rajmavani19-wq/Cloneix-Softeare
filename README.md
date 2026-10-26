<div align="center">

# 🧬 Cloneix

### Clone Any Website — Pixel Perfect, One Click

Transform any URL into a production-ready Next.js codebase with true 1:1 visual fidelity.
Powered by Headless Chromium, CSS inlining, and intelligent asset extraction.

[![Next.js](https://img.shields.io/badge/Next.js-16.3-black?logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)](https://react.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4-06B6D4?logo=tailwindcss)](https://tailwindcss.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)

</div>

---

## ✨ Features

| Feature | Description |
|:---|:---|
| **🎯 1:1 Pixel-Perfect Cloning** | Real Headless Chromium captures computed CSS, fonts, images, and layouts for exact visual fidelity |
| **📦 CSS Inlining Engine** | All external stylesheets (`@font-face`, `@media`, `@keyframes`) are inlined directly into the HTML |
| **🌐 Live Preview** | View your cloned websites in a full desktop-width iframe — exactly as the original looks |
| **📥 .ZIP Export** | Download standalone, production-ready Next.js 16 + Tailwind CSS v4 source code packages |
| **📁 Folder Workspaces** | Organize projects into color-coded folders with real-time project counts |
| **🔐 Secure Auth** | Email + password authentication with NextAuth.js and encrypted sessions |
| **🌙 Dark / Light Mode** | Seamless theme switching across all pages |
| **📱 Responsive Dashboard** | Full-featured dashboard with sidebar navigation, project management, and settings |
| **📧 Contact Form** | Contact submissions stored directly in MongoDB |

---

## 🛠️ Tech Stack

| Layer | Technology |
|:---|:---|
| **Framework** | Next.js 16.3 (App Router) |
| **UI Library** | React 19.2 |
| **Language** | TypeScript 5 |
| **Styling** | Tailwind CSS v4 + shadcn/ui |
| **Database** | MongoDB + Mongoose 9 |
| **Authentication** | NextAuth.js v5 (beta) |
| **Web Scraping** | Puppeteer 25 (Headless Chromium) |
| **HTML Parsing** | Cheerio |
| **Animations** | Motion (Framer Motion) |
| **Icons** | Lucide React |
| **Email** | Nodemailer |
| **Archive** | JSZip |

---

## 📁 Project Structure

```
cloneix/
├── src/
│   ├── app/
│   │   ├── page.tsx                 # Landing page
│   │   ├── layout.tsx               # Root layout + metadata
│   │   ├── globals.css              # Global styles + Tailwind
│   │   ├── login/                   # Login page
│   │   ├── register/                # Registration page
│   │   ├── about/                   # About Us page
│   │   ├── privacy/                 # Privacy Policy page
│   │   ├── terms/                   # Terms & Conditions page
│   │   ├── contact/                 # Contact Us page
│   │   ├── dashboard/
│   │   │   ├── page.tsx             # Dashboard home (projects list)
│   │   │   ├── layout.tsx           # Dashboard layout + sidebar
│   │   │   ├── projects/[id]/       # Project detail + preview
│   │   │   ├── folders/[id]/        # Folder detail page
│   │   │   ├── live-view/           # Live clone preview (desktop)
│   │   │   └── settings/            # User settings
│   │   ├── api/
│   │   │   ├── auth/                # NextAuth API routes
│   │   │   ├── projects/            # CRUD + clone + export APIs
│   │   │   ├── folders/             # Folder management APIs
│   │   │   ├── contact/             # Contact form API
│   │   │   └── proxy/               # Asset proxy for cloned sites
│   │   └── clones/                  # Static cloned site pages
│   ├── components/
│   │   ├── ui/                      # shadcn/ui components
│   │   ├── animations.tsx           # Reusable motion animations
│   │   ├── theme-provider.tsx       # Dark/light theme provider
│   │   └── theme-toggle.tsx         # Theme switch component
│   ├── lib/
│   │   ├── cloner-service.ts        # Core cloning engine (Puppeteer + CSS inlining)
│   │   ├── db.ts                    # MongoDB connection
│   │   ├── auth.ts                  # NextAuth configuration
│   │   └── utils.ts                 # Utility functions
│   ├── models/                      # Mongoose schemas (User, Project, Folder, Contact)
│   ├── hooks/                       # Custom React hooks
│   └── types/                       # TypeScript type definitions
├── public/                          # Static assets
├── package.json
├── tsconfig.json
├── next.config.ts
├── postcss.config.mjs
├── eslint.config.mjs
└── .env.local                       # Environment variables
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 24
- **MongoDB** (local or Atlas cloud)
- **npm** or **yarn**

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/cloneix.git
cd cloneix
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env.local` file in the project root:

```env
# MongoDB Connection
MONGODB_URI=mongodb://localhost:27017/cloneix

# NextAuth Secret (generate a random string for production)
AUTH_SECRET=your-secret-key-here

# App URL
AUTH_URL=http://localhost:3000
```

### 4. Start Development Server

```bash
npm run dev
```

Open **http://localhost:3000** in your browser.

---

## 📋 Available Scripts

| Command | Description |
|:---|:---|
| `npm run dev` | Start development server (Webpack) |
| `npm run build` | Create production build |
| `npm start` | Start production server |
| `npm run lint` | Run ESLint |
| `npm run typecheck` | Run TypeScript type checking |
| `npm run check` | Run lint + typecheck + build |

---

## 🔄 How It Works

```
┌─────────────┐     ┌──────────────────┐     ┌─────────────────┐     ┌──────────────┐
│  Enter URL  │ ──▶ │  Headless Chrome  │ ──▶ │  CSS Inlining   │ ──▶ │  Live Clone  │
│             │     │  (Puppeteer)      │     │  Engine         │     │  Preview     │
└─────────────┘     └──────────────────┘     └─────────────────┘     └──────────────┘
                            │                         │                       │
                            ▼                         ▼                       ▼
                    • Execute JavaScript      • Inline all CSS        • Full desktop
                    • Capture DOM             • Resolve fonts          preview iframe
                    • Extract assets          • Fix image paths       • .ZIP download
                    • Network idle wait       • Patch animations      • Folder organize
```

1. **URL Input** → User enters a website URL in the dashboard
2. **Chromium Extraction** → Puppeteer launches headless Chrome, navigates to the URL, waits for network idle, and captures the fully-rendered DOM
3. **CSS Inlining** → All external CSS stylesheets are fetched and inlined as `<style>` blocks, including `@font-face`, `@media` queries, and `@keyframes` animations
4. **Asset Resolution** → Relative image/font/script paths are converted to absolute URLs via a proxy
5. **Storage** → The complete HTML with inlined CSS is stored in MongoDB
6. **Preview** → A dedicated API serves the raw HTML for pixel-perfect iframe rendering
7. **Export** → Users can download the full clone as a standalone Next.js + Tailwind CSS project in a .ZIP archive

---

## 🔐 Authentication Flow

- Users register with **email + password**
- Passwords are hashed with **bcrypt**
- Sessions are managed by **NextAuth.js v5** with JWT strategy
- Protected routes redirect unauthenticated users to `/login`

---

## 🗄️ Database Models

| Model | Description |
|:---|:---|
| **User** | Email, hashed password, profile settings |
| **Project** | Clone URL, extracted HTML, status, metadata |
| **Folder** | Name, color, associated project references |
| **Contact** | Name, email, message from contact form |

---

## 🎨 UI Components

Built with **shadcn/ui** component library:
- Button, Card, Badge, Dialog, Input, Select, Textarea
- Custom animations with **Motion** (Framer Motion)
- Theme toggle (dark/light) with **next-themes**
- Responsive sidebar navigation

---

## 📄 Pages

| Page | Route | Description |
|:---|:---|:---|
| Landing | `/` | Hero, features, how-it-works, FAQ, CTA |
| Login | `/login` | Email + password sign in |
| Register | `/register` | New account registration |
| Dashboard | `/dashboard` | Project list, create new clone |
| Project Detail | `/dashboard/projects/[id]` | Preview, settings, export |
| Live View | `/dashboard/live-view` | Full desktop preview of clones |
| Folders | `/dashboard/folders/[id]` | Folder contents view |
| Settings | `/dashboard/settings` | User profile settings |
| About | `/about` | About the platform |
| Privacy | `/privacy` | Privacy Policy |
| Terms | `/terms` | Terms & Conditions |
| Contact | `/contact` | Contact form |

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the **MIT License**.

---

<div align="center">

**Built with Cloneix using Next.js 16, React 19, and Tailwind CSS v4**

**[Cloneix](http://localhost:3000)** — Clone Any Website, Instantly.

</div>

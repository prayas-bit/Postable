<div align="center">

```
██████╗  ██████╗ ███████╗████████╗ █████╗ ██████╗ ██╗     ███████╗
██╔══██╗██╔═══██╗██╔════╝╚══██╔══╝██╔══██╗██╔══██╗██║     ██╔════╝
██████╔╝██║   ██║███████╗   ██║   ███████║██████╔╝██║     █████╗  
██╔═══╝ ██║   ██║╚════██║   ██║   ██╔══██║██╔══██╗██║     ██╔══╝  
██║     ╚██████╔╝███████║   ██║   ██║  ██║██████╔╝███████╗███████╗
╚═╝      ╚═════╝ ╚══════╝   ╚═╝   ╚═╝  ╚═╝╚═════╝ ╚══════╝╚══════╝
```

**A Next.js prototype wired up to AWS — built fast, deployed live.**

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![AWS](https://img.shields.io/badge/AWS-integrated-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://postable-aws-prototype-zeta.vercel.app)

[🚀 Live Demo](https://postable-aws-prototype-zeta.vercel.app/)) · [🐛 Report Bug](https://github.com/prayas-bit/postable-aws-prototype/issues) · [✨ Request Feature](https://github.com/prayas-bit/postable-aws-prototype/issues)

</div>

---

## 🗂️ What is this?

**Postable** is a full-stack prototype that connects a slick Next.js frontend to AWS cloud infrastructure. It serves as a working proof-of-concept for building post-centric applications (think social feeds, content publishing, or async messaging) backed by AWS services — all wrapped in a modern TypeScript/Next.js App Router setup.

---

## ⚡ Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | Next.js 15 (App Router) |
| **Language** | TypeScript |
| **Styling** | Tailwind CSS + shadcn/ui |
| **Cloud** | AWS (SDK integrated) |
| **Auth / Middleware** | Custom `middleware.ts` |
| **Deployment** | Vercel |

---

## 🏗️ Project Structure

```
postable-aws-prototype/
├── app/                  # Next.js App Router pages & layouts
├── lib/                  # Shared utilities, AWS clients, helpers
├── middleware.ts          # Route middleware (auth guards, redirects)
├── components.json        # shadcn/ui component config
├── test-aws.js           # AWS integration smoke tests
├── test-li.js            # LinkedIn / external API tests
├── next.config.ts         # Next.js configuration
└── tsconfig.json          # TypeScript configuration
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+
- **npm / yarn / pnpm / bun**
- An **AWS account** with the appropriate credentials configured

### 1 — Clone

```bash
git clone https://github.com/prayas-bit/postable-aws-prototype.git
cd postable-aws-prototype
```

### 2 — Install dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3 — Configure environment

Create a `.env.local` file in the root and add your AWS credentials and any other required secrets:

```env
AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key

# Add any other project-specific env vars here
```

> ⚠️ **Never commit `.env.local` to version control.** It's already in `.gitignore`.

### 4 — Run the dev server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. The app hot-reloads as you edit `app/page.tsx`.

---

## 🧪 Running Tests

Smoke-test your AWS and external API connections:

```bash
# Test AWS connectivity
node test-aws.js

# Test external integrations
node test-li.js
```

---

## ☁️ Deployment

The easiest path is one-click deploy via **Vercel**:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/prayas-bit/postable-aws-prototype)

Don't forget to set your environment variables in the Vercel project dashboard under **Settings → Environment Variables**.

---

## 🛠️ Development Notes

- **Font optimization** is handled via [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) using the [Geist](https://vercel.com/font) family.
- **Route protection** lives in `middleware.ts` — modify it to adjust auth rules.
- AWS client initialization is centralized in `lib/` — add new service clients there.
- UI components are managed via [shadcn/ui](https://ui.shadcn.com/) (`components.json`).

---

## 📚 Resources

- [Next.js Docs](https://nextjs.org/docs)
- [AWS SDK for JavaScript (v3)](https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/)
- [shadcn/ui](https://ui.shadcn.com/)
- [Vercel Deployment Docs](https://nextjs.org/docs/app/building-your-application/deploying)

---

## 📄 License

This project is open source. Feel free to fork, extend, and build on top of it.

---

<div align="center">

Made with ☕ and way too many AWS console tabs

</div>

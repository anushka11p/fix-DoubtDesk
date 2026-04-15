# Contributing to DoubtDesk

First off, thank you for considering contributing to DoubtDesk! 🎉

Every contribution matters — whether it's fixing a typo, improving the UI, or building a new feature.

---

## 📋 Table of Contents

- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Branch Naming](#branch-naming)
- [Commit Message Format](#commit-message-format)
- [Pull Request Process](#pull-request-process)
- [Code Style Guidelines](#code-style-guidelines)
- [Issue Labels](#issue-labels)
- [Need Help?](#need-help)

---

## 🚀 Getting Started

1. **Fork** the repository on GitHub.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/<your-username>/DoubtDesk.git
   cd DoubtDesk
   ```
3. **Install dependencies:**
   ```bash
   npm install
   ```
4. **Set up environment variables:**
   ```bash
   cp .env.example .env
   ```
   Fill in the API keys (see README for details).
5. **Run the dev server:**
   ```bash
   npm run dev
   ```

---

## 🤝 How to Contribute

### Find an Issue

- Browse the [Issues](https://github.com/knoxiboy/DoubtDesk/issues) tab.
- Look for labels: `good-first-issue`, `beginner-friendly`, `enhancement`, `bug`.
- **Comment** on the issue to let others know you're working on it.

### No Issue Exists?

- If you found a bug or have an idea, **open a new issue first**.
- Describe the problem/feature clearly.
- Wait for maintainer approval before starting work on large features.

---

## 🔧 Development Workflow

```
1. Fork the repo
2. Create a feature branch from `main`
3. Make your changes
4. Test locally (npm run dev)
5. Commit with a clear message
6. Push to your fork
7. Open a Pull Request
```

---

## 🌿 Branch Naming

Use descriptive, prefixed branch names:

| Prefix | Use Case | Example |
| :--- | :--- | :--- |
| `feature/` | New feature | `feature/add-search-to-doubts` |
| `fix/` | Bug fix | `fix/classroom-invite-code-validation` |
| `docs/` | Documentation | `docs/add-screenshots-to-readme` |
| `style/` | UI/styling changes | `style/improve-mobile-sidebar` |
| `refactor/` | Code refactoring | `refactor/extract-doubt-card-component` |

---

## 💬 Commit Message Format

Follow the [Conventional Commits](https://www.conventionalcommits.org/) style:

```
<type>: <short description>
```

**Types:**

| Type | When to Use |
| :--- | :--- |
| `feat` | Adding a new feature |
| `fix` | Fixing a bug |
| `docs` | Documentation changes |
| `style` | UI/CSS changes (no logic change) |
| `refactor` | Code restructuring |
| `test` | Adding or updating tests |
| `chore` | Build, config, or tooling changes |

**Examples:**
```
feat: add loading skeleton to classroom page
fix: prevent duplicate join on invite code submission
docs: add contribution guide
style: fix mobile alignment on doubt cards
```

---

## 📬 Pull Request Process

1. **Ensure your branch is up to date** with `main`:
   ```bash
   git checkout main
   git pull upstream main
   git checkout your-branch
   git rebase main
   ```

2. **Create the PR** against the `main` branch.

3. **PR title** should follow the commit format:
   ```
   feat: add search functionality to public doubts page
   ```

4. **PR description** should include:
   - What the change does
   - Related issue number (e.g., `Closes #12`)
   - Screenshots (if UI changes)

5. **Wait for review** — maintainers will review within 48 hours.

6. **Address feedback** — push additional commits to the same branch.

---

## 🎨 Code Style Guidelines

### TypeScript
- Avoid `any` types wherever possible. Use proper interfaces.
- Use `const` by default; `let` only when reassignment is needed.

### React / Next.js
- Use functional components with hooks.
- Keep components focused — one component per file.
- Place reusable components in `/components`.
- Place page-specific logic in `/app/<route>/page.tsx`.

### Styling
- Use **Tailwind CSS** exclusively (match the existing dark theme).
- Follow the existing color palette: slate-950 backgrounds, blue-500/600 accents.
- Maintain glassmorphism patterns (backdrop-blur, border-white/10).

### File Organization
- API routes: `/app/api/<feature>/route.ts`
- Components: `/components/<ComponentName>.tsx`
- Shared utilities: `/lib/<utility>.ts`
- Database schema: `/configs/schema.ts`
- Utility scripts: `/scripts/<script>.ts`

---

## 🏷️ Issue Labels

| Label | Description |
| :--- | :--- |
| `good-first-issue` | Simple, well-scoped. Perfect for first contribution. |
| `beginner-friendly` | Slightly more involved, still approachable. |
| `bug` | Something is broken. |
| `enhancement` | New feature or improvement. |
| `documentation` | README, guides, comments. |
| `frontend` | UI components, pages, styling. |
| `backend` | API routes, database, server logic. |
| `ai` | AI prompts, models, moderation. |
| `help-wanted` | Maintainer needs help on this. |

---

## ❓ Need Help?

- **Comment on the issue** — maintainers will respond.
- **Open a Discussion** — for broader questions or ideas.
- **Check existing PRs** — someone may have already started similar work.

---

Thank you for making DoubtDesk better! 🚀

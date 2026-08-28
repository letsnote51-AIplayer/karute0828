# Nail Salon Customer Chart UI Mock Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create four smartphone-only, high-fidelity screens for a 10–15 second social-media demo of a nail salon customer-understanding chart.

**Architecture:** Use a small Vite React app with fixed fictional data and React Router navigation. No persistence, CRUD, backend, API, or production data logic is included; only route transitions and save feedback needed for filming are interactive.

**Tech Stack:** React, TypeScript, Vite, React Router, Tailwind CSS, Lucide React

**Spec:** `docs/superpowers/specs/2026-08-28-nail-salon-customer-chart-design.md`

## Global Constraints

- Build a UI mock, not a production application.
- Use fictional customer data and rights-safe nail images only.
- Optimize for 390×844px and support widths from 375px through 430px.
- Do not create desktop or tablet-specific layouts; center a maximum-width 480px mobile canvas on wider screens.
- Do not add localStorage, database, API, authentication, CRUD, uploads, or real search logic.
- Optimize the hero path for a 10–15 second screen recording.
- Do not deploy or publish.

## File Map

```text
src/
  app/App.tsx
  components/AppShell.tsx
  components/CustomerCard.tsx
  components/SafetyAlert.tsx
  components/SaveToast.tsx
  data/demoData.ts
  pages/DashboardPage.tsx
  pages/CustomerListPage.tsx
  pages/CustomerDetailPage.tsx
  pages/ConversationEditPage.tsx
  styles/index.css
  main.tsx
public/images/
```

---

### Task 1: Visual Foundation and Fixed Data

**Files:**
- Create: `package.json`, `vite.config.ts`, `tsconfig.json`, `index.html`
- Create: `src/main.tsx`, `src/app/App.tsx`, `src/components/AppShell.tsx`
- Create: `src/data/demoData.ts`, `src/styles/index.css`, `public/images/*`

**Produces:** Running Vite app, smartphone shell, routes, design tokens, and fictional content.

- [ ] Create the React, TypeScript, Vite, React Router, Tailwind CSS, and Lucide React project.
- [ ] Define ivory, greige, charcoal, taupe, burgundy, deep-green, border, and muted-text tokens.
- [ ] Build a fixed mobile bottom navigation, compact top header, 44px minimum touch targets, and 48px primary actions.
- [ ] Add the approved 佐藤 美咲 profile plus five secondary fictional customers.
- [ ] Add rights-safe nail images and avatar placeholders with useful alt text.
- [ ] Configure `/`, `/customers`, `/customers/customer-001`, and `/customers/customer-001/edit`.
- [ ] Run `npm run build`; expect TypeScript and Vite to finish with exit code 0.
- [ ] Commit with `git commit -m "chore: scaffold customer chart UI mock"`.

### Task 2: Four Recording Screens

**Files:**
- Create: `src/components/CustomerCard.tsx`, `src/components/SafetyAlert.tsx`, `src/components/SaveToast.tsx`
- Create: `src/pages/DashboardPage.tsx`, `src/pages/CustomerListPage.tsx`
- Create: `src/pages/CustomerDetailPage.tsx`, `src/pages/ConversationEditPage.tsx`
- Modify: `src/app/App.tsx`, `src/styles/index.css`

**Produces:** Complete four-screen recording path with visual save feedback.

- [ ] Build the dashboard with metrics, recent customers, recent nail photos, and a film-ready `佐藤` search field.
- [ ] Make its search action navigate to the fixed result screen; do not implement general search.
- [ ] Build the result screen with 佐藤 美咲 first, visible tags, last visit, visit count, staff, and warning state.
- [ ] Build the customer chart in this order: identity, safety warning, preferences, nail condition, conversation, service notes, nail photos, timeline.
- [ ] Show `アクリル系商材に注意` using an icon, heading, and text—not color alone.
- [ ] Build the fixed conversation edit screen with the approved copy and Save/Cancel controls.
- [ ] Make Save show `カルテを保存しました` for about two seconds, then return to the customer chart; do not persist text.
- [ ] Use 150–250ms transitions for content, panels, and toast feedback.
- [ ] Run `npm run build`; expect exit code 0.
- [ ] Commit with `git commit -m "feat: build customer chart recording screens"`.

### Task 3: Smartphone Polish and Recording Check

**Files:**
- Modify: `src/styles/index.css`, `src/components/AppShell.tsx`, all four pages as needed
- Create: `README.md`

**Produces:** Recording-ready smartphone compositions.

- [ ] Verify 375×812: one column, fixed bottom navigation, horizontal photo row, full-screen edit, and no page-level horizontal overflow.
- [ ] Verify 390×844: primary recording composition, thumb-reachable actions, and safety warning visible immediately after opening the chart.
- [ ] Verify 430×932: cards expand naturally without overly long text lines.
- [ ] Verify a wider browser window shows the same mobile canvas centered at maximum width 480px without a desktop sidebar.
- [ ] Complete dashboard search → result → warning → preferences/conversation → edit → save toast.
- [ ] Confirm the flow records in 10–15 seconds without waiting or dead ends.
- [ ] Confirm all content and images are fictional or rights-safe.
- [ ] Confirm unavailable features are absent or clearly marked as demo-only.
- [ ] Document `npm install`, `npm run dev`, and `npm run build`, plus a warning not to enter real customer data.
- [ ] Run `npm run build`; expect exit code 0 and a generated `dist/` directory.
- [ ] Commit with `git commit -m "style: polish responsive recording mock"`.

## Completion Gate

- Four approved screens exist.
- Smartphone layouts at 375px, 390px, and 430px are visually verified.
- The 10–15 second recording path works.
- Save feedback appears without implying real persistence.
- No real personal data or unlicensed assets are present.
- No backend, localStorage, CRUD, authentication, deployment, or production integration was added.

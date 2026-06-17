# Gridion — Complete Build Plan

## 1. PRODUCT

Gridion is an automation-first pipeline builder for creative agencies. It replaces the scattered mix of Slack threads, Notion docs, Trello boards, and email chains that 5–50 person design, branding, content, and video studios use to shepherd client work from intake to delivery. Users build a visual pipeline of stages (Lead → Brief → Concept → Revision → Approval → Delivered), drop client projects onto it, and wire automations that move a project forward, notify the right person, or create a recurring task when a stage changes. The core value is that the agency stops dropping balls: every project has a current stage, a next step, an owner, and a due date — visible in one calm view. The primary user is the ops lead or founder of a small agency who is the de facto PM for 8–25 concurrent projects and is allergic to tools that feel like a second job. Research frames the underlying pain precisely: the average team loses work to manual handoff and "we set it up and forgot about it" syndrome — Gridion's pipeline is designed to make a stalled project the loudest thing on the screen, not a hidden detail in a spreadsheet.

## 2. WHO IT'S FOR

**Primary ICP:** Ops lead, head of production, or founder at a 5–50 person creative agency (branding, design, content, video, motion) running 8–25 concurrent client projects. They are the de facto PM. They opened this app because they missed a deadline or lost a status update again.

**Secondary ICP:** Senior account manager at a 20–100 person agency who needs a shared view across producers.

**How the ICP shapes the product and tone:**
- **Time-poor, low-patience** → the dashboard opens on a single "Today" view with exactly one primary CTA ("Add project" or "Move forward on stalled work"). No nested menus deeper than two clicks from home.
- **Allergic to enterprise bloat** → the tone is peer-to-peer, calm, expert. No "supercharge your workflows." No fake testimonials, customer logos, user counts, or star ratings. Honest copy only.
- **Multi-tenant by design** → every agency is its own workspace; pipeline stages and templates are scoped per workspace, not per user.
- **Collaborative but solo-starter** → signup creates the user + a personal workspace; they can invite teammates later from settings. No empty "add your team" nag screens blocking the core flow.
- **Visual buyers** → the pipeline is a real drag/click kanban, not a list. Creatives think in stages, not rows.

## 3. LOOK & FEEL

### Visual system

**Vibe / positioning:** Calm, airy, editorial. Reads like a thoughtful product magazine, not a SaaS landing page. The brand promise — "your agency's nervous system, in one quiet view" — is delivered through restraint: lots of whitespace, soft gradients, low-contrast hierarchy, no aggressive CTAs, no neon.

**Color palette (Calm System):**
- `--sky-50: #F0F8FC` (page tint on marketing)
- `--sky-100: #D9EDF7` (hover backgrounds, borders)
- `--sky-300: #7CC4E8` (illustrations, accent strokes)
- `--sky-600: #3A93C0` (interactive accents on dark)
- `--sky-700: #2C7DA0` (primary text on light, links)
- `--mint-100: #DBF3E8` (success backgrounds)
- `--mint-300: #88D4B5` (success accents, completed stages)
- `--mint-600: #2E8B6E` (success text)
- `--sand-100: #F7EFE0` (warm card backgrounds, soft alerts)
- `--sand-300: #E8D5B0` (illustration fills)
- `--sand-600: #B89968` (secondary text accent)
- `--paper: #FAFAF7` (soft white base)
- `--ink: #1F2A37` (primary text)
- `--ink-2: #4A5568` (secondary text)
- `--ink-3: #8A94A6` (tertiary text, icons)
- `--line: #ECE9E2` (hairline borders)

**Typography:**
- `Geist` (variable) for UI, body, labels, numbers, buttons.
- `Lora` (variable) for editorial moments: landing H1, section headlines, testimonial-style quotes, the empty-state headline in the dashboard.
- Sizes: H1 56/64, H2 40/48, H3 28/36, H4 20/28, body 16/26, small 14/22, micro 12/18.
- Tracking: tight on display headings (-0.02em), normal elsewhere.
- Numbers in dashboards use `tabular-nums`.

**Spacing & layout:**
- 8px base. Sections separated by 96–128px on marketing, 32–48px in dashboard.
- Max content width 1200px on marketing, 1280px in dashboard.
- Generous left/right padding (px-6 mobile, px-10 tablet, px-16 desktop).
- Cards: 16px radius, `border: 1px solid var(--line)`, `box-shadow: 0 1px 2px rgba(31,42,55,0.04)`. On hover: `0 4px 16px rgba(31,42,55,0.06)`.
- Buttons: 12px radius, 44px tall, padding 16/20, font-medium 15/20.

**Iconography:** Lucide icons, 1.5px stroke, 18–20px default, never filled. Stage icons in pipeline are outline.

**Imagery:** Soft, slightly desaturated product illustrations (gradient blobs in sky/mint, line-art of pipeline nodes). No stock photos of handshakes. Empty states use 1:1 SVG illustrations in sand/sky.

**Interaction / motion:**
- Hover: 150ms ease-out, slight 2px translate-y, shadow lift.
- Page transitions: 200ms fade.
- Drag in kanban: 120ms ease-out lift to 1.02 scale, 1px shadow.
- No bouncing, no springy easing. Easing tokens: `--ease-out: cubic-bezier(0.16, 1, 0.3, 1)`.
- Focus rings: 2px mint-300 with 2px offset, never default browser blue.

### Marketing landing page (top to bottom)

**Navigation bar (sticky, blurred, 72px tall):**
- Left: `Gridion` wordmark in Geist 600 18px, with a small 14px sky-300 dot before the "i".
- Center: Features, How it works, Pricing, Templates (anchor links).
- Right: `Sign in` (ghost button) + `Start free` (primary button, sky gradient).
- On scroll: 8px frosted background (`rgba(250,250,247,0.85)` + `backdrop-blur 12px`), hairline bottom border.

**Hero (min 640px, two-column on desktop, stacked on mobile):**
- Left column:
  - Eyebrow chip: `For creative agencies` in sand-100 bg, ink-2 text, 12px uppercase, 8px radius, dot prefix.
  - H1 in Lora 56/64, ink: `The pipeline your agency should have had three years ago.`
  - Sub in Geist 18/30, ink-2, max 540px: `Stop losing work in Slack threads and Trello cards. Gridion turns your client pipeline into one calm, automated flow — from lead to delivered.`
  - Primary CTA: `Start free` (sky gradient pill, white text) + secondary `See a sample pipeline` (mint outline pill, links to `/templates` and opens a public sample).
  - Trust line below CTAs (honest, no fake numbers): `A workspace for your agency, in under 60 seconds. No credit card.`
- Right column:
  - Soft gradient background (sky-50 → mint-100 → paper, 600x520 blob).
  - A 2D illustration of a 5-column pipeline with 8 card thumbnails, one card pulsing with a mint glow and a "moved to Review" automation badge. Cards have rounded corners, soft shadows, tiny avatars.
  - Subtle floating sparkles (4–5 dot SVGs).

**Features section (`Everything your agency needs, nothing it doesn't.`):**
- 6 feature cards in a 3x2 grid (2x3 on tablet, 1 column on mobile).
- Each card: 24px Lora icon container (sky-100 bg), 24px H4 title in ink, 16/26 body in ink-2, 1 hairline border, 16px radius.
- Features (in order, no marketing fluff):
  1. **Visual pipelines** — Build your client stages once. Drag projects forward, not Trello tickets.
  2. **Stage automations** — When a project hits "Approved," auto-create the delivery task and notify the account lead.
  3. **Templates that work** — Start from a Branding pipeline, a Video pipeline, or a Content pipeline. Clone and edit.
  4. **Honest deadlines** — A stalled project gets louder, not quieter. Red dot on the dashboard the day after due.
  5. **One inbox per stage** — Comments and files live on the project card, not scattered across email.
  6. **Built for small teams** — Five to fifty people, one workspace, no enterprise seat math.

**How it works section (4 steps, alternating left-right on desktop):**
- H2 Lora: `Four steps. One calm Monday morning.`
- Steps, each with a 1:1 illustration, step number in Lora 48px sand-300:
  1. **Create your workspace.** Sign up, name your agency, pick a starter template or start blank.
  2. **Set your stages.** Defaults: Lead, Brief, Concept, Revision, Approval, Delivered. Rename anything.
  3. **Add projects and assign owners.** Drop a project in, type the client, pick a stage, set a due date.
  4. **Wire automations.** Click any stage → "When a project enters here, do…" — choose from a real list.
- Subtle connecting line between steps in sky-100.

**Pricing section (3 tiers, no fake "most popular" badges, no strikethroughs):**
- H2 Lora: `Honest pricing. No per-seat nonsense.`
- Sub: `One workspace, one flat price. Invite as many people as your agency has.`
- Three cards on a 3-column grid (stacked on mobile), middle card elevated 8px with sky-100 border (this is the "Studio" tier — visually balanced, not "popular"):
  - **Solo** — Free forever — Up to 3 active projects, 1 workspace, all core pipeline features. For freelancers and founders trialing.
  - **Studio** — $39/month — Unlimited projects, unlimited teammates, stage automations (up to 10 active), file comments, public read-only pipeline share link. For 5–30 person agencies.
  - **Agency** — $129/month — Everything in Studio, unlimited automations, multiple pipelines per workspace, custom stage fields, CSV export, priority support. For 30+ person agencies.
- Each card: name (Lora 24), one-line description (Geist 14 ink-2), 5–6 bullet features with sky-300 check icons, primary button (sky gradient for Studio, mint outline for Solo and Agency), no hidden footnote.
- Below the grid, a small honest FAQ-ish line: `Switch tiers any time. Annual billing is two months free. No card required to start.`

**CTA section (centered, sand-100 → paper gradient background):**
- Lora H2: `Your next project is already late. Start a pipeline.`
- Two buttons: `Start free` (primary sky) + `See a sample pipeline` (ghost).
- Below, microcopy: `No credit card. One workspace. Cancel any time.`

**Footer (3-column grid, ink-3 text, paper bg, 64px top padding):**
- Col 1: `Gridion` wordmark + 1-line description + copyright.
- Col 2: Product — Features, Templates, Pricing, Changelog (link `#` with `Soon` pill, never a dead link).
- Col 3: Company — About, Privacy, Terms, Contact (mailto).
- Honest placeholder note for Changelog until v1 ships.

### Auth pages (sign-in / sign-up)

**Layout:** Centered single card on paper bg, 24px from top. Above the card: Gridion wordmark + a Lora H2 (`Welcome back` or `Set up your agency in 60 seconds`).

**Sign-up card (440px wide):**
- Fields: Full name, Agency name, Work email, Password (with strength hint), Confirm password.
- Helper: `We use this to name your workspace. You can change it later.`
- Primary button: `Create workspace` (full width, sky gradient).
- Below button: `By continuing, you agree to our Terms and Privacy.` (terms/privacy are placeholders, no dead links — use `#` with `Soon` pill on the marketing site, real stub pages in the app footer are NOT in scope here).
- Footer link: `Already have an account? Sign in` (mint-600).

**Sign-in card (400px wide):**
- Fields: Email, Password.
- Primary button: `Sign in`.
- Below: `Forgot password?` (mint-600 link, opens a modal that calls Supabase `resetPasswordForEmail` and shows a "check your inbox" state).
- Footer link: `New here? Create a workspace` (mint-600).

**Loading state:** Replace button text with a sky-300 spinner, disable form.
**Error state:** Inline message in sand-300 bg with ink text above the button, never a red alert toast.
**Success state:** Brief mint-100 banner "Check your inbox to verify" (sign-up) before redirect.

### Dashboard

**Layout shell (`/dashboard/layout.tsx`):**
- Left sidebar, 240px, paper bg, hairline right border.
- Top bar, 64px, white bg, hairline bottom border, contains: page title (Lora 22), breadcrumb (Geist 14 ink-3), and right-side user menu (avatar circle with initials, click to open dropdown: Settings, Sign out).
- Main content area, padded 32px, max-width 1280px, centered.

**Sidebar contents:**
- Top: `Gridion` wordmark + small "Workspace: {agencyName}" line.
- Section `Workspace`: Home, Projects, Templates.
- Section `Account`: Settings.
- Bottom: usage card (small, sand-100 bg) showing `{n} of {limit} active projects` for the user's tier. Honest, no upsell copy.

**Home / Metrics page (`/dashboard`):**
- Page header: `Good {morning|afternoon|evening}, {first name}.` (Lora 28) + sub in ink-2: `{n} active projects · {m} due this week`.
- Stat cards row (4 cards, equal width):
  1. **Active projects** — count, sky-300 icon, sparkline-style inline bar (real data from Supabase, no fake numbers).
  2. **Due this week** — count, mint-300 icon if 0, sand-300 icon if 1+ in danger.
  3. **Stalled** — count of projects not moved in 7+ days, sand-300 icon, red dot if > 0.
  4. **Completed (30d)** — count, mint-300 icon.
- Two-column grid below:
  - Left (2/3): **Needs attention** list — projects with closest due dates or oldest "last moved" timestamps. Each row: project name (ink), client (ink-3), stage badge, due date (red text if overdue, sand-300 if due in ≤2 days), "Move forward" button on hover (calls a small action menu: Move to next stage, Add note, Set reminder). Empty state: small sky-300 illustration + `Everything is on track. Take a coffee.`
  - Right (1/3): **Recent activity** — vertical timeline of last 10 events (project created, stage changed, automation fired, comment added). Each entry: 8px colored dot by event type, text, relative time (`2h ago`).

**Projects pipeline page (`/dashboard/projects`):**
- Page header: `Projects` (Lora 28) + right-side controls: view toggle (Pipeline / List, default Pipeline), filter chip (Stage, Owner, Due), `New project` primary button (sky gradient).
- **Pipeline view (default):** Horizontal-scroll kanban with columns for each stage (Lead, Brief, Concept, Revision, Approval, Delivered). Column header: stage name (Geist 14 medium ink), count badge (sky-100 bg), `+ Add project` icon button (only on Lead column). Cards: 280px wide, white bg, 12px radius, hairline border, hover lift. Card content: project name (ink 15 medium), client (ink-3 13), due date chip (sand-100 if due soon, sand-300 bg if overdue, mint-100 if delivered), owner avatar (24px), small automation count badge if any. Click card → `/dashboard/projects/[id]`. Drag card to another column → calls `moveProject` server action, which writes a `stage_changed` activity.
- **List view:** Table with columns: Project, Client, Stage, Owner, Due, Last moved. Sort by Due default, ascending.
- Empty state: if no projects, show sky-300 illustration + `No projects yet. Add your first one — it takes 20 seconds.` + `New project` button.

**New project modal (used by both views, opens from `+ Add project` or `New project`):**
- Fields: Project name (required), Client (required), Stage (default Lead, dropdown of workspace stages), Owner (dropdown of workspace members, defaults to current user), Due date (date picker, optional), Notes (textarea, optional).
- Footer: `Cancel` ghost + `Create project` primary. On submit, inserts row, closes modal, scrolls to the new card with a 1.5s mint glow.

**Project detail page (`/dashboard/projects/[id]`):**
- Two-column layout (2/3 main, 1/3 side):
  - Main:
    - Header: project name (Lora 28) editable inline, client (ink-3), stage badge with dropdown to move.
    - Tabs (Geist 14 medium, sky-700 underline for active): Overview, Files, Activity.
    - **Overview tab:** description (markdown-light rendering, paragraphs only, no images), checklist (add/remove/check items), files section stub (real UI: drag-and-drop placeholder with "Files coming soon" honest message), comments (text input, submits to `comments` table).
    - **Files tab:** Honest empty state with upload UI disabled and a "Files upload is on the Studio plan and above" message if on Solo. (We don't fake uploads.)
    - **Activity tab:** Full timeline of all events for this project, with actor, type, time.
  - Side:
    - **Details card:** Owner, Due date, Created date, Stage entered dates.
    - **Automations card:** list of automations attached to this project (e.g., "When stage → Delivered, send email to client"). Each has an edit and remove.
    - **Move card:** large primary button `Move to {next stage}` + secondary dropdown for any other stage.

**Templates page (`/dashboard/templates`):**
- Page header: `Templates` (Lora 28) + sub: `Save your pipeline as a template, or start from one of ours.`
- Tabs: `Workspace templates` (user-created) and `Starter templates` (system-provided, read-only).
- Grid of template cards (3 columns on desktop, 2 tablet, 1 mobile). Each card: 1:1 sand-100 illustration with a tiny pipeline sketch, name (Lora 20), description (Geist 14 ink-2), 5 stage chips, footer: `Use template` primary button.
- `Use template` opens a modal: `Create from "{name}"` → fields: pipeline name (defaults to template name), create. On submit, clones the template's stages and automations into a new pipeline.
- Workspace templates can be edited (name, description, stages, automations) via the same editor as a pipeline.
- Starter templates include: `Branding sprint` (Lead → Brief → Concept → Revision → Approval → Delivered), `Content calendar` (Idea → Drafting → Review → Scheduled → Published), `Video production` (Pre-pro → Shoot → Edit → Review → Final → Delivered), `Client retainer` (Active → Weekly report → Renewal → Paused).

**Pipeline / template editor (`/dashboard/templates/[id]` or new pipeline):**
- Left rail: list of stages with drag handles, `+ Add stage` button at bottom.
- Center: horizontal stage column preview with 3 sample cards per stage.
- Right rail: stage details panel (name, color, default owner, automations).
- Automations section: per-stage, a list of `When {event} on this stage, then {action}` rules. For v1, supported events: `project enters stage`, `project leaves stage`, `project stuck in stage for X days`. Supported actions: `send notification to {member}`, `create a task {name} assigned to {member}`, `move to {stage}`, `add comment {text}`. Add automation opens a clean 3-step form. No code, no JSON.

**Settings page (`/dashboard/settings`):**
- Tabs: `Profile`, `Workspace`, `Members`, `Billing`.
- **Profile:** Full name (input), Avatar initials (auto from name, read-only), Email (read-only, link to change via Supabase), Time zone (select).
- **Workspace:** Agency name, Default pipeline, Time zone, Sign-out everywhere button.
- **Members:** Table of current members (avatar, name, email, role: Owner / Member, last active). Owner can invite by email (sends a Supabase magic-link style invite — we use the `inviteUserByEmail` flow with email+password set on first visit), change role, remove. Empty state if solo.
- **Billing:** Current plan (card with name, price, "Active since {date}"), `Manage subscription` button (placeholder linking to a real `/dashboard/settings/billing` stub page with a "Stripe is not connected in this environment" honest message — no fake checkout).

## 4. USER FLOWS

### Flow 1: Discover → sign up → first pipeline
1. Land on `/`. Read hero. Click `Start free`.
2. Sign-up form opens. Enter name, agency, email, password.
3. Server action `signUp` calls `supabase.auth.signUp({ email, password, options: { data: { full_name, agency_name } } })`. Supabase sends a confirmation email (or auto-confirms in dev).
4. On success, client `signIn` is called to start a session, then router pushes to `/dashboard`.
5. `/dashboard` loads: empty state with `Welcome, {name}. Create your first project.` + `Use a starter template` and `Start blank` buttons.
6. User clicks `Use a starter template` → templates modal opens with the 4 starter templates.
7. Pick `Branding sprint` → modal "Create from Branding sprint" → name input → submit.
8. Server action `createPipelineFromTemplate` inserts a new pipeline with the 6 stages and any default automations. Then pushes to `/dashboard/projects` with the new empty pipeline.
9. Click `+ Add project` on the Lead column. Modal opens. Fill name, client, owner, due date. Submit. Card appears in the Lead column with a brief mint glow.

### Flow 2: Move a project + automation fires
1. On `/dashboard/projects`, drag a card from Concept to Revision. On drop, client calls `moveProject(id, "Revision")` server action.
2. Server action updates `projects.stage`, writes an `activities` row, evaluates any automations bound to the old and new stages.
3. If an automation matches (`project leaves Concept → send notification to ops`), the server action inserts a `notifications` row (bell icon in top bar would be the next iteration; for v1, we just write the row and show a toast `Automation fired: notified ops lead`).
4. Card re-renders in the Revision column. Stage change is visible to the user immediately. Activity appears in the project detail Activity tab.

### Flow 3: Add an automation
1. Open pipeline editor for a pipeline (e.g., from a workspace template).
2. Click the Revision stage in the left rail. Right panel opens.
3. Click `+ Add automation`. A 3-step modal appears:
   - Step 1: When — radio buttons: `Project enters this stage`, `Project leaves this stage`, `Project stuck here for 3+ days`. (Default: enters.)
   - Step 2: Then — radio buttons: `Notify {member}`, `Create task assigned to {member}`, `Move to {stage}`, `Add comment {text}`. Each shows the relevant inputs.
   - Step 3: Confirm — shows a summary in Lora 18: `When a project enters Revision, notify {member}.`
4. Submit. The automation appears in the stage's right panel as a chip with edit / delete. Toast `Automation saved.`

### Flow 4: Settings — invite a teammate
1. User goes to `/dashboard/settings` → Members tab.
2. Clicks `Invite member`. Modal: email input, role select (Member default).
3. Submit calls `inviteUserByEmail`. Supabase sends a magic link that lands on `/auth/callback?next=/onboarding/accept`.
4. The accept page shows: `Set your password to finish joining {agency}.` Email pre-filled, password + confirm fields, full name. On submit, the user is added to the workspace's `members` table and signed in.

### Flow 5: Forgot password
1. On `/sign-in`, click `Forgot password?`. Modal opens with single email field.
2. Submit calls `resetPasswordForEmail(email, { redirectTo: '/auth/callback?next=/dashboard/settings' })`.
3. Modal state changes to: `Check {email} for a reset link. The link expires in 1 hour.`
4. User clicks the link → lands on `/auth/callback` → middleware exchanges code for session → redirected to `/dashboard/settings?reset=1`.
5. A banner on Settings: `Set a new password` with a form to update.

### States
- **Loading:** Suspense boundaries with a 64px sky-300 spinner in a centered flexbox. No skeletons on the marketing site (instant feel). Skeletons in dashboard list views: 3 rows of 56px gray bars.
- **Empty:** Always an illustration + Lora headline + Geist body + 1 primary CTA. Never a "no data" message alone.
- **Error:** Sand-300 bg, ink-2 text, friendly copy: `We couldn't load your projects. Refresh, or try again.` + `Retry` button. Never red alerts.
- **Success toasts:** Top-right, mint-100 bg, ink text, slide-in 200ms, auto-dismiss 3s.

## 5. PAGES / ROUTES

| Route | Type | Purpose | Main UI |
|---|---|---|---|
| `/` | Public | Marketing landing | Nav, Hero, Features, How it works, Pricing, CTA, Footer |
| `/sign-in` | Public | Auth | Centered sign-in card |
| `/sign-up` | Public | Auth | Centered sign-up card |
| `/forgot-password` | Public | Auth | Centered reset request |
| `/auth/callback` | Public route handler | Supabase auth code exchange | Server-side code → session → redirect to `next` param |
| `/auth/confirm` | Public route handler | Email confirmation | Server-side verify → redirect |
| `/onboarding/accept` | Auth required | Accept invite | Set password + name form |
| `/dashboard` | Auth required | Home / metrics | Header, stat cards, attention list, activity |
| `/dashboard/projects` | Auth required | Pipeline | Header, filters, kanban or list view |
| `/dashboard/projects/[id]` | Auth required | Project detail | Tabs: Overview, Files, Activity + side cards |
| `/dashboard/templates` | Auth required | Templates list | Tabs: Workspace, Starter, grid of cards |
| `/dashboard/templates/[id]` | Auth required | Pipeline / template editor | Stage rail, preview, automations panel |
| `/dashboard/settings` | Auth required | Settings | Tabs: Profile, Workspace, Members, Billing |
| `/dashboard/settings/billing` | Auth required | Billing stub | Plan card, honest "Stripe not connected" panel |
| `/api/projects` | API | POST create, GET list | JSON |
| `/api/projects/[id]` | API | PATCH update, DELETE | JSON |
| `/api/projects/[id]/move` | API | PATCH stage | JSON, runs automations |
| `/api/templates` | API | POST create, GET list | JSON |
| `/api/templates/[id]/use` | API | POST clone | JSON |
| `/api/members/invite` | API | POST invite | JSON |
| `/404` | Public | Not found | Lora headline `This page is not in your pipeline.` + `Back to dashboard` (if authed) or `Back home` |
| `/500` | Public | Server error | Same pattern, gentler copy |

All authenticated pages export `export const dynamic = 'force-dynamic'`. No `dynamic = 'error'`.

## 6. CORE FEATURES

1. **Workspaces (multi-tenant).** Every signup creates a `workspace` row. All projects, pipelines, templates, members are scoped by
# Progress Tracker

Update this file whenever the current phase, active feature, or implementation state changes.

## Current Phase

- In progress

## Current Goal

- Feature 03 (TBD — check feature-specs for next spec)

## Completed

- **01-design-system**: shadcn/ui installed and configured (new-york style, Tailwind v4, cssVariables). Components added: Button, Card, Dialog, Input, Tabs, Textarea, ScrollArea. `lucide-react` installed. `lib/utils.ts` created with `cn()`. Dark theme tokens defined in `globals.css` via `@theme inline`. `npm run build` passes.
- **02-editor**: Editor chrome components created. `components/editor/editor-navbar.tsx` — fixed top navbar with sidebar toggle using `PanelLeftOpen`/`PanelLeftClose` icons, dark background with bottom border. `components/editor/project-sidebar.tsx` — floating overlay sidebar (does not push content), slides in from left via CSS transform, accepts `isOpen`/`onClose` props, Projects header + close button, shadcn Tabs (My Projects / Shared) with empty placeholder states, full-width New Project button with Plus icon. `npm run build` passes.

## In Progress

- None.

## Next Up

- Feature 03 (TBD — check feature-specs)

## Open Questions

- None yet.

## Architecture Decisions

- Tailwind v4 used via `@import "tailwindcss"` with `@theme inline` for CSS variable mapping (no tailwind.config.js).
- Dark-only theme enforced with `@variant dark (false)` — CSS variables are defined at `:root` without a `.dark` class toggle.
- shadcn/ui new-york style chosen; components in `components/ui/` must not be modified (per ai-workflow-rules.md).
- `radix-ui` (unified package) used instead of individual `@radix-ui/react-*` packages — this is how shadcn v4.6 installs Radix.

## Session Notes

- Next.js 16.2.4 + React 19.2.4 + Tailwind v4. No tailwind.config.js — all theme tokens live in globals.css.
- shadcn v4.6.0 installed components non-interactively via `npx shadcn@latest add ... --yes` after creating components.json manually.
- clsx, tailwind-merge, class-variance-authority needed to be installed separately (shadcn did not auto-add them to package.json).

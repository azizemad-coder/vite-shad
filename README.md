## Vite + React + TypeScript + Tailwind v4 + shadcn/ui

A modern React starter powered by Vite 7, TypeScript, Tailwind CSS v4, and [shadcn/ui](https://ui.shadcn.com) (Radix UI + utility CSS). It comes preconfigured with aliases, theming, and a curated set of UI components under `src/components/ui`.

### Features
- **Vite 7**: fast dev server and HMR
- **React 19 + TypeScript**: latest JSX and type safety
- **Tailwind CSS v4**: configured via `src/index.css` and `@tailwindcss/vite`
- **shadcn/ui**: accessible components built on **Radix UI**
- **Lucide icons**, **react-hook-form + zod**, and **sonner** toasts
- **Path alias `@`**: maps to `src` for clean imports

### Requirements
- **Node**: 18+ (LTS recommended)
- **Package manager**: pnpm (preferred)

### Quick start
```bash
pnpm install
pnpm dev
```

### Scripts
- **dev**: start Vite dev server
- **build**: type-check and build for production
- **preview**: preview the production build
- **lint**: run ESLint

```bash
pnpm dev
pnpm build
pnpm preview
pnpm lint
```

### Using shadcn/ui components
Preinstalled components live in `src/components/ui`. Import with the `@` alias:

```tsx
import { Button } from "@/components/ui/button"

export function Example() {
  return <Button>Click me</Button>
}
```

Add more components with the CLI (reads `components.json`):

```bash
npx shadcn@latest add alert-dialog accordion card dialog dropdown-menu input select tabs tooltip
```

### Theming and Tailwind
- Tailwind v4 is configured in `src/index.css` using `@import "tailwindcss"` and design tokens.
- Dark mode uses the `.dark` class and custom properties; toggle by adding/removing `.dark` on the root element.
- Optional: wrap your app with `next-themes` to handle theme persistence.

```tsx
import { ThemeProvider } from "next-themes"

<ThemeProvider attribute="class" defaultTheme="system" enableSystem>
  <App />
</ThemeProvider>
```

### Aliases
`@` → `src` (see `tsconfig.app.json`). Example: `@/lib/utils` and `@/components/ui/*`.

### Project structure
```text
src/
  components/
    ui/               # shadcn/ui components
  hooks/
  lib/
    utils.ts
  index.css          # Tailwind v4 + theme tokens
components.json       # shadcn/ui configuration
```

### Credits
- [Vite](https://vitejs.dev)
- [Tailwind CSS v4](https://tailwindcss.com)
- [shadcn/ui](https://ui.shadcn.com)
- [Radix UI](https://www.radix-ui.com)

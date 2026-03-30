# Portfolio Project Documentation

## Overview
This project is a personal portfolio web application built with React, TypeScript, and Vite. It uses Tailwind CSS for styling and shadcn/ui (Radix-based components) for reusable UI elements.

The app is structured as a single-page application (SPA) with page-based components such as About, Achievements, Certificates, and Contact.

## Tech Stack
- **Framework / Runtime:** React 18
- **Language:** TypeScript
- **Build Tool:** Vite
- **Styling:** Tailwind CSS
- **UI Components:** shadcn/ui + Radix UI
- **Routing:** React Router DOM
- **Animation:** Framer Motion
- **Testing:** Vitest + Testing Library
- **Hosting:** Firebase Hosting

## Project Structure
```text
portfolio/
  public/                 # Static assets (robots, sitemap, verification files)
  src/
    assets/               # Images and asset files
    components/           # Shared app components
      ui/                 # shadcn/ui component library
    hooks/                # Custom React hooks
    lib/                  # Utility helpers
    pages/                # Route/page components
    test/                 # Test setup and test files
    App.tsx               # Root app component
    main.tsx              # App entry point
    index.css             # Global styles
  firebase.json           # Firebase Hosting config
  vite.config.ts          # Vite configuration
  tailwind.config.ts      # Tailwind configuration
  vitest.config.ts        # Vitest configuration
```

## Prerequisites
Install the following before running locally:
- **Node.js** (recommended: latest LTS)
- **npm** (comes with Node.js)

Check versions:
```bash
node -v
npm -v
```

## Installation
```bash
# 1. Go to project directory
cd portfolio

# 2. Install dependencies
npm install
```

## Available Scripts
Defined in `package.json`:

- `npm run dev` - Start local dev server
- `npm run build` - Build production bundle into `dist/`
- `npm run build:dev` - Build in development mode
- `npm run preview` - Preview built app locally
- `npm run lint` - Run ESLint checks
- `npm run test` - Run tests once (Vitest)
- `npm run test:watch` - Run tests in watch mode

## Local Development
Run the development server:
```bash
npm run dev
```

Vite will output a local URL (typically `http://localhost:5173`).

## Production Build
Create optimized production files:
```bash
npm run build
```

Preview production build locally:
```bash
npm run preview
```

## Testing
Run all tests once:
```bash
npm run test
```

Run tests continuously:
```bash
npm run test:watch
```

## Linting
Run lint checks:
```bash
npm run lint
```

## Firebase Deployment
This project is configured for Firebase Hosting.

Current hosting setup in `firebase.json`:
- Hosting target site: `tharun-port`
- Deploy directory: `dist`
- SPA rewrite: all routes rewrite to `index.html`

### Deploy Steps
```bash
# 1. Build app
npm run build

# 2. Login to Firebase (if needed)
firebase login

# 3. Deploy hosting
firebase deploy --only hosting
```

## Configuration Files
- `vite.config.ts` - Vite bundling and plugin configuration
- `tailwind.config.ts` - Tailwind theme/content settings
- `postcss.config.js` - PostCSS plugins
- `eslint.config.js` - Lint rules
- `vitest.config.ts` - Test runner config
- `tsconfig*.json` - TypeScript compiler setup

## Main Pages
Located in `src/pages/`:
- `Index.tsx`
- `About.tsx`
- `Achievements.tsx`
- `Certificates.tsx`
- `Contact.tsx`
- `NotFound.tsx`

## Notes for Contributors
- Keep shared UI elements in `src/components/`.
- Keep route-level content in `src/pages/`.
- Reuse utilities from `src/lib/utils.ts`.
- Add tests under `src/test/` for new functionality.

## Troubleshooting
- If dependencies fail: delete `node_modules` and lockfile, then run `npm install` again.
- If build fails: run `npm run lint` and `npm run test` to locate issues.
- If deployed route returns 404: ensure Firebase rewrite rule is present and app is built to `dist`.

## License
Add your preferred license information here (for example, MIT).

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- **Install dependencies**: `pnpm install`
- **Development server**: `pnpm dev` (hot-reload enabled)
- **Production build**: `pnpm build` (includes type-checking)
- **Type checking**: `pnpm type-check`
- **Linting**: `pnpm lint` (auto-fixes issues)
- **Code formatting**: `pnpm format`
- **Unit tests**: `pnpm test:unit` (uses Vitest)
- **Preview build**: `pnpm preview`

## Architecture

This is a Vue 3 frontend application using the Composition API with TypeScript support.

### Tech Stack
- **Vue 3** with Composition API
- **TypeScript** for type safety
- **Vite** for build tooling and development server
- **Vue Router** for client-side routing
- **Pinia** for state management
- **Vitest** for unit testing with jsdom environment
- **ESLint + Prettier** for code quality

### Project Structure
- `src/main.ts` - Application entry point, sets up Vue app with Pinia and router
- `src/router/index.ts` - Route definitions with lazy loading for About page
- `src/stores/` - Pinia stores (uses Composition API pattern)
- `src/views/` - Page-level components
- `src/components/` - Reusable components with `__tests__/` subdirectory
- `src/assets/` - Static assets and global CSS

### Key Conventions
- Uses `@` alias for `src/` directory imports
- Pinia stores use Composition API pattern with `defineStore()`
- Components follow Vue 3 Composition API style
- Tests are co-located with components in `__tests__/` directories
- Package manager is **pnpm** (not npm or yarn)
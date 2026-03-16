# Copilot Instructions for Soc Ops

## Mandatory Development Checklist

- [ ] Run `npm run lint`
- [ ] Run `npm run build`
- [ ] Run `npm test`

## Project

- React 19 + TypeScript + Vite social bingo app.
- Client-only; no backend, API, or SSR.
- Main flow: start screen, board, bingo state.

## Architecture

- Keep screen orchestration in `src/App.tsx`.
- Keep game state, persistence, and flow in `src/hooks/useBingoGame.ts`.
- Keep bingo rules and board logic in `src/utils`.
- Keep prompt content in `src/data/questions.ts`.
- Keep UI components presentational under `src/components`.

## Working Rules

- Prefer simple typed function components.
- Preserve the split between pure logic and React state.
- Preserve localStorage behavior unless the task changes saved-state UX.
- Reuse Tailwind v4 theme tokens from `src/index.css` before adding new ones.
- Prefer utility classes over custom CSS unless styles need sharing.
- Keep layouts compact and mobile-friendly.
- Update `src/utils/bingoLogic.test.ts` when gameplay logic changes.
- Keep edits targeted and avoid changing `package-lock.json` unless dependencies change.

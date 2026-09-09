# HYMatch

A mobile-first medical matching game with concise teaching pearls after each correct connection.

## Modes

- Solo
- Duel on one device
- Online room mode when a shared realtime backend is configured

## Local development

```bash
npm install
npm run dev
```

## Tests

```bash
npm test
```

## GitHub Pages

The project is configured for a repository named `HYMatch` and uses `base: "/HYMatch/"` in Vite.

The included workflow builds and deploys the site to GitHub Pages. Repository Pages settings may need to use **GitHub Actions** as the source.

## Online rooms

GitHub Pages is static hosting, so cross-device multiplayer needs shared storage. HYMatch supports two backends:

1. `window.storage`, when hosted in an environment that provides it.
2. Firebase Realtime Database through `VITE_FIREBASE_DATABASE_URL`.

Without either backend, Solo and Duel remain fully available and the online setup is disabled rather than failing at runtime.

### Firebase note

The database must permit the reads/writes your deployment needs. Do not put private server credentials in this repository. Firebase client configuration/database URLs are normally public; secure the database with appropriate Firebase rules.

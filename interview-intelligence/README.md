# Interview Intelligence

AI-powered candidate evaluation tool built on the Coral platform.

## Setup

```bash
npm install
npm run dev
```

Open http://localhost:5173

## Stack

- React 18 + Vite
- Recharts (radar/area charts)
- Lucide React (icons)
- Anthropic API (AI suggestions, inconsistency detection, report generation)

## Key files

- `src/App.jsx` — entire application (single-file architecture)

## Notes

- The Anthropic API key is handled by the Claude.ai artifact environment.
  When running locally, add your key to the `claude()` fetch call in App.jsx:
  ```js
  headers: {
    "Content-Type": "application/json",
    "x-api-key": "YOUR_ANTHROPIC_KEY",
    "anthropic-version": "2023-06-01",
    "anthropic-dangerous-direct-browser-access": "true",
  }
  ```

- ElevenLabs TTS will work locally (no CSP restriction outside Claude.ai).
  Add your key to the `elevenKey` useState default value in InterviewScreen.

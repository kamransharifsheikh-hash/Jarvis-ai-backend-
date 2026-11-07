# JARVIS AI Backend

Deploy this folder as a Node Web Service.

- Build command: `npm install`
- Start command: `npm start`
- Health check path: `/health`

Set `OPENAI_API_KEY` and `GEMINI_API_KEY` in your hosting provider's secret/environment-variable settings. Never commit keys or place them in the Android APK.

`POST /chat` body:
`{"message":"Hello","language":"ur-PK","provider":"auto"}`

`provider` can be `auto`, `openai`, or `gemini`. Auto tries OpenAI first, then Gemini if OpenAI fails and a Gemini key is configured.

Free Render web services sleep after 15 minutes idle, so the first request after sleep may be slow. This starter has rate limiting but not user authentication; add per-user authentication before public release.

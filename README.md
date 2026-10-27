# Riella AI

Riella is a custom AI chat website configured by Mariella Arao. This version uses a secure Vercel serverless endpoint and the Google Gemini API.

## Deploy

1. Upload `index.html`, the `api` folder, `README.md`, and `.gitignore` to your GitHub repository. **Never upload your API key.**
2. In Vercel, choose **Add New → Project** and import the `riella-ai` GitHub repository.
3. Select framework **Other** if asked. Leave build command empty and output directory at default.
4. In **Environment Variables**, add `GEMINI_API_KEY` and paste the secret value from Google AI Studio. Set it for Production (and Preview if desired).
5. Deploy, then visit your Vercel URL and send a test message.

## Important limitations

- The Fast/Balanced/Deep setting changes maximum response length; it does not switch model or guarantee deeper reasoning.
- Chat history and personality are stored only in each browser's local storage. There is no login or cross-device sync.
- The API is public to anyone with the website URL. **Before sharing widely**, add durable rate limiting, abuse controls, monitoring, and spending safeguards. Free-tier quotas are limited and may change.
- Gemini free-tier requests may be used by the provider to improve its products, subject to applicable terms. Do not send confidential information; add a clear privacy notice and review provider policies before inviting others.
- This starter supports text chat only. It does not provide live web browsing, file analysis, or persistent model training.
- To develop locally, use `vercel dev` with an environment variable configured; opening index.html directly will not reach `/api/chat`.

# Orbit — Personal AI Companion Starter

A mobile-first, private-first PWA prototype for Android browsers.

## Included now
- Responsive home screen
- Demo chat UI (not connected to an AI model)
- Local tasks and user-controlled memories
- Export/delete local data
- Permission hierarchy preview
- PWA manifest and service worker for offline shell caching

## Important limitations
- This is a starter prototype, not a compiled Android APK.
- Voice, cloud AI, background monitoring, notifications, and phone-control tools are not connected.
- Data is stored in browser localStorage and is not encrypted by this prototype. Do not save sensitive data.
- Never put an API key in `index.html` or a mobile client. Add a backend before connecting an AI provider.
- Do not grant unrestricted device, banking, messaging, file-system, or terminal access to an agent.

## Try it on your Android phone
1. Extract this ZIP.
2. Host the folder on a trusted HTTPS static host (or run it from a local development server).
3. Open the HTTPS page in Chrome on Android.
4. Use Chrome's menu → **Add to Home screen** / **Install app** if offered.

For service-worker/offline installation, use HTTPS or localhost; opening the file directly may not enable PWA installation.

## Recommended next build step
Add a small FastAPI backend with one model provider, explicit per-tool permissions, request logging, timeouts, rate limits, and a kill switch. Keep secrets on the backend, not in the phone app.

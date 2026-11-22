# SafeHer
A privacy-conscious, mobile-first safety companion for trusted contacts, SOS preparation, and journey check-ins.

## Features
- Responsive landing page and safety dashboard
- Local trusted contact management with click-to-call
- SOS confirmation demo; manual emergency call and local event notice
- Journey timer persisted using timestamps, check-in, extension, and cancel
- Explicit user-triggered browser location with Google Maps link
- India emergency resource page and display-name settings
- Accessible keyboard focus, reduced-motion support, mobile navigation

## Stack
React, Vite, TypeScript, React Router, Lucide React, CSS, browser LocalStorage and Geolocation APIs.

## Install and run
```sh
npm install
npm run dev
```

## Production build
```sh
npm run build
npm run preview
```
Build output is `dist`. No environment variables or backend are required.

## Deploy to Vercel
1. Push this project to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Keep the detected Vite defaults (build command `npm run build`, output `dist`).
4. Deploy. The included `vercel.json` rewrites SPA routes to the app entry point.

## Privacy
Contacts, display name, and active journey are stored only in this browser's local storage. Location is requested only after the user presses the location or SOS control. No location history, analytics, account, or server upload is used. Clear local data in Settings.

## Demo limitations
SafeHer does not send SMS, email, push notifications, or automatic alerts. SOS is a local demo; browser sharing only invokes the native share sheet and does not confirm delivery. It never calls emergency services automatically. The app does not replace official emergency services.

## Browser limitations
Geolocation generally requires HTTPS or localhost and depends on browser permission and device support. Web Share and clipboard availability varies. Browser timers may not run while the app is closed; journey reminders are not background monitoring. Emergency features requiring connectivity may not work offline.

## Roadmap
Optional installable PWA shell, focused unit tests, richer journey history, and user-controlled map visualization.

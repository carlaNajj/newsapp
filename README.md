## Mobile News App

This is a simple mobile‑friendly news application built with **Vue 3**, **TypeScript**, **Vite**, and **Capacitor**.  
It fetches top headlines from the GNews API and allows searching and limiting the number of articles.

> **Note**: You must provide a valid GNews API key for the app to work.

## Prerequisites

- **Node.js** (recommended LTS, e.g. 18+)
- **npm** (comes with Node)
- A **GNews API key**

## 1. Install dependencies

Open a terminal in the project root (`mobileNewsApp`) and run:

```bash
npm install
```

## 2. Configure your GNews API key

For local development, the key is currently hard‑coded in `src/components/Articles.vue` as `GNEWS_API_KEY`.  
Replace the placeholder value with your own key:

```ts
const GNEWS_API_KEY = 'YOUR_API_KEY_HERE';
```

(Optionally, you can later move this to an environment variable using `import.meta.env`.)

## 3. Run the app in the browser (Vite dev server)

Still in the project root, start the dev server:

```bash
npm run dev
```

Then follow the URL shown in the terminal (usually `http://localhost:5173/`) in your browser.

## 4. Run on a mobile device/emulator with Capacitor (optional)

### iOS

```bash
npm run build
npx cap sync ios
npx cap open ios
```

Then build and run the app from Xcode on a simulator or a real device.

### Android

```bash
npm run build
npx cap sync android
npx cap open android
```

Then build and run the app from Android Studio on a simulator or a real device.

## 5. Build for production (web)

To create an optimized production build of the web app:

```bash
npm run build
```

The compiled files will be placed in the `dist` folder.

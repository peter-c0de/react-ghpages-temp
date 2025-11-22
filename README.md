# STEPS in a Nutshell:

1. Install gh-pages: npm install --save-dev gh-pages
2. Update vite.config.js
3. Update package.json
4. Deploy: npm run deploy

PS: MUST USE gh-pages branch on GitHub Pages.

______________

# Aliases for Linux Users:

alias reactVite='npx create-vite@latest'

alias reactRun='npm run dev'

alias reactIghp='npm install --save-dev gh-pages'

alias reactDeploy='npm run deploy'

______________


# STEPS:

## 🛠 Step 1: Install gh-pages
npm install --save-dev gh-pages
______________

## 🧠 Step 2: Update vite.config.js
Edit vite.config.js and add the base option:

import { defineConfig } from 'vite';

import react from '@vitejs/plugin-react';



export default defineConfig({

  base: '/my-vite-app/', // 👈 Must match your repo name

  plugins: [react()],

});
______________


## 📦 Step 3: Update package.json
Here’s the full example of what your package.json should include:

{

  "name": "my-vite-app",

  "version": "1.0.0",

  "private": true,

  "homepage": "https://your-username.github.io/my-vite-app",

  "scripts": {

    "dev": "vite",

    "build": "vite build",

    "preview": "vite preview",

    "predeploy": "npm run build",

    "deploy": "gh-pages -d dist"

  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },

  "devDependencies": {

    "@vitejs/plugin-react": "^4.0.0",

    "vite": "^5.0.0",

    "gh-pages": "^6.0.0"

  }

}

Replace "homepage" with your actual GitHub Pages URL.

______________

## 🚀 Step 4: Deploy to GitHub Pages
npm run deploy

This will:

•	Build your app into the dist/ folder

•	Push it to the gh-pages branch on GitHub

•	Your site will be live at: https://your-username.github.io/my-vite-app/






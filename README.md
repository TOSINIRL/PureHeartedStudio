# Netlify Deployment Guide

This guide explains how to deploy your projects from GitHub to Netlify for automated, continuous deployment.

---

## 🚀 Overview
Deploying your project from GitHub to Netlify is like setting up an automated pipeline: once it's linked, every time you push code to GitHub, Netlify automatically updates your live site. It’s one of the smoothest workflows in web development.

---

## Phase 1: Connect Your GitHub Account
1.  **Log in to Netlify**: Go to [app.netlify.com](https://app.netlify.com) and sign in. (Pro tip: Sign in using your GitHub account to save time on authorization later).
2.  **Start a New Project**: On your team dashboard, click the **Add new site** button and select **Import an existing project**.
3.  **Choose Your Provider**: Click the **GitHub** button. A popup will appear asking for permission.
    *   *Note: You can choose to give Netlify access to all your repositories or just selected ones. For better security, picking only the repos you need is a solid move.*

## Phase 2: Select and Configure
1.  **Pick Your Repo**: Search for the repository you want to deploy and click on it.
2.  **Basic Settings**:
    *   **Branch to deploy**: Usually `main` or `master`. This is the branch Netlify watches for changes.
    *   **Base directory**: Leave this blank unless your frontend code is inside a subfolder (like a monorepo).
3.  **Build Settings**: Netlify is pretty smart—it usually auto-detects your framework (React, Vue, Vite, etc.).
    *   **Build command**: Usually something like `npm run build` or `yarn build`.
    *   **Publish directory**: This is where your compiled files live. For Vite it's `dist`, for React it's `build`, and for Next.js it’s usually `.next`.

## Phase 3: The Big Launch
1.  **Click "Deploy [Project Name]"**: Netlify will start the build process. You can click on the "Production deploys" log to watch the "cooking" in real-time.
2.  **Claim Your URL**: Once the status turns to Published, you’ll see a randomly generated URL (like `sparkly-unicorn-12345.netlify.app`).
3.  **Change the Name**: Don't like the random name? Go to **Site configuration > Site details > Change site name** to give it a custom sub-domain.

---

## 💡 Pro-Tips for a Smoother Deploy
*   **Environment Variables**: If your code uses API keys (like `.env` files), go to **Site configuration > Environment variables** and add them there. Netlify won't see your local `.env` file because it's (hopefully!) ignored by Git.
*   **Continuous Deployment**: From now on, you don't need to touch Netlify. Just `git push` to your `main` branch, and your site will update automatically in about 30–60 seconds.

---
*Based on content from [IRLMEDIA](https://tosinirl.github.io/IRLMEDIA/)*

# Fashion Atelier CRM

A static web CRM for Fashion Atelier — hosted on Netlify, version-controlled on GitHub.

## 🚀 Live Site

> Your Netlify URL will appear here after first deploy.

## 📁 Project Structure

```
/
├── index.html          # Main CRM app
├── netlify.toml        # Netlify config & redirect rules
├── .gitignore          # Git ignore rules
└── .github/
    └── workflows/
        └── deploy.yml  # Auto-deploy on push to main
```

## 🛠️ Setup & Deployment

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/fashion-atelier-crm.git
git push -u origin main
```

### 2. Connect to Netlify

1. Go to [netlify.com](https://netlify.com) → **Add new site** → **Import from Git**
2. Select your GitHub repo
3. Build settings are auto-detected from `netlify.toml`
4. Click **Deploy site**

### 3. Add GitHub Secrets (for CI/CD auto-deploy)

In your GitHub repo → **Settings** → **Secrets and variables** → **Actions**, add:

| Secret Name | Where to find it |
|---|---|
| `NETLIFY_AUTH_TOKEN` | Netlify → User Settings → Personal Access Tokens |
| `NETLIFY_SITE_ID` | Netlify → Site Settings → General → Site ID |

After this, every push to `main` will auto-deploy to Netlify.

## ✅ Features

- Single-file static app — no build step needed
- Auto-deploys on every `git push`
- All routes redirect to `index.html` (SPA-friendly)

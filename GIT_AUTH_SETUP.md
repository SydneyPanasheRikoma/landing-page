# Git Authentication Setup Guide

## Option 1: Personal Access Token (Recommended)

1. **Create a Personal Access Token:**
   - Go to GitHub.com → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Click "Generate new token (classic)"
   - Give it a name (e.g., "landing-page-project")
   - Select scopes: `repo` (full control of private repositories)
   - Click "Generate token"
   - **Copy the token immediately** (you won't see it again!)

2. **Use the token for authentication:**
   ```bash
   git push -u origin main
   ```
   When prompted:
   - Username: `SydneyPanasheRikoma`
   - Password: `[paste your token here]`

## Option 2: GitHub CLI (gh)

1. **Install GitHub CLI** (if not installed)
2. **Authenticate:**
   ```bash
   gh auth login
   ```
3. **Then push:**
   ```bash
   git push -u origin main
   ```

## Option 3: SSH Key (Most Secure)

1. **Generate SSH key** (if you don't have one):
   ```bash
   ssh-keygen -t ed25519 -C "31242177@vupune.ac.in"
   ```

2. **Add SSH key to GitHub:**
   - Copy your public key: `cat ~/.ssh/id_ed25519.pub`
   - Go to GitHub.com → Settings → SSH and GPG keys → New SSH key
   - Paste your public key

3. **Change remote to SSH:**
   ```bash
   git remote set-url origin git@github.com:SydneyPanasheRikoma/landing-page.git
   ```

4. **Push:**
   ```bash
   git push -u origin main
   ```

## Quick Push (After Authentication)

Once authenticated, you can push all remaining files:

```bash
cd "C:\Users\fahad\Documents\Site projects\SS4ED"
git add .
git commit -m "Add remaining files: styles.css, script.js, .gitignore, FIGMA_ACCESS_NOTES.md"
git push -u origin main
```
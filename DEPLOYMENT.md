# 🚀 GitHub Pages Deployment Instructions

Follow these steps to host your Socure presentation on GitHub Pages:

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **"+"** icon in the top-right corner
3. Select **"New repository"**
4. Configure your repository:
   - **Repository name**: `SamplePOV`
   - **Description**: "Interactive Socure POC presentation"
   - **Visibility**: Choose Public or Private
   - **DO NOT** initialize with README (we already have one)
5. Click **"Create repository"**

## Step 2: Push Your Code to GitHub

After creating the repository, GitHub will show you commands. Use these commands:

```bash
cd /home/claude/SamplePOV

# Add your GitHub repository as remote (replace YOUR-USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR-USERNAME/SamplePOV.git

# Rename branch to main (optional but recommended)
git branch -M main

# Push to GitHub
git push -u origin main
```

**Note**: When prompted for credentials:
- Username: Your GitHub username
- Password: Use a **Personal Access Token** (not your GitHub password)
  - Create one at: https://github.com/settings/tokens
  - Required scopes: `repo`

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **"Settings"** tab
3. Click **"Pages"** in the left sidebar
4. Under **"Source"**:
   - Branch: Select `main`
   - Folder: Select `/ (root)`
5. Click **"Save"**

## Step 4: Access Your Live Presentation

After a few minutes, your presentation will be live at:

```
https://YOUR-USERNAME.github.io/SamplePOV/
```

GitHub will display the exact URL in the Pages settings.

## 🔄 Updating Your Presentation

To update the presentation after making changes:

```bash
cd /home/claude/SamplePOV

# Make your changes to index.html, then:
git add .
git commit -m "Update presentation"
git push
```

Changes will be live within 1-2 minutes.

## 🎨 Customization Tips

- Edit `index.html` to update content, data, or styling
- Replace client name, dates, and metrics as needed
- Update charts with actual client data
- Customize colors in the CSS if needed

## 📱 Sharing Your Presentation

Once live, you can:
- Share the URL with clients and prospects
- Present directly from the browser
- Works on desktop, tablet, and mobile devices
- Use keyboard arrows to navigate during presentations

## 🔒 Making Repository Private

If you created a public repository but want it private:

1. Go to repository **Settings**
2. Scroll to **"Danger Zone"**
3. Click **"Change repository visibility"**
4. Select **"Make private"**

**Note**: GitHub Pages is available for private repos on GitHub Pro, Team, or Enterprise plans.

## ❓ Troubleshooting

**Pages not working?**
- Wait 5-10 minutes after enabling Pages
- Check that `index.html` is in the root directory
- Verify branch name is correct in Pages settings

**Need to use a different branch?**
- Create a `gh-pages` branch
- Push your code to that branch
- Select `gh-pages` in Pages settings

**Authentication issues?**
- Use a Personal Access Token instead of password
- Make sure token has `repo` scope

---

Need help? Check [GitHub Pages documentation](https://docs.github.com/en/pages)

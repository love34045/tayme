# GitHub Pages Deployment Guide

This guide will walk you through the steps to deploy your TayMe jewelry website to GitHub Pages.

## Step 1: Create a New GitHub Repository

1. Go to [GitHub](https://github.com/) and sign in to your account
2. Click the "+" button in the top right corner and select "New repository"
3. Name your repository (e.g., "tayme-jewelry" or simply "tayme")
4. Make sure the repository is set to "Public" (GitHub Pages requires this for free accounts)
5. Click "Create repository"

## Step 2: Upload Files to GitHub

### Option 1: Upload via Browser

1. In your new repository, click the "uploading an existing file" link
2. Drag and drop all files and folders from this directory
3. Click "Commit changes"

### Option 2: Upload via Git (Advanced)

If you're familiar with Git:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/[your-username]/[repository-name].git
git push -u origin main
```

## Step 3: Configure GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to the "GitHub Pages" section (or click on "Pages" in the sidebar)
4. Under "Source", select "Deploy from a branch"
5. For "Branch", select "main" and "/ (root)"
6. Click "Save"

## Step 4: Verify Deployment

1. GitHub will show you the URL where your site is published (usually `https://[username].github.io/[repository-name]/`)
2. It may take a few minutes for your site to be deployed
3. Visit the URL to verify your site is working correctly

## Step 5: Add a Custom Domain (Optional)

If you have your own domain name:

1. In the GitHub Pages settings, enter your domain in the "Custom domain" field
2. Click "Save"
3. Create a CNAME record with your domain registrar pointing to `[username].github.io`
4. Wait for DNS propagation (can take up to 48 hours)

## Troubleshooting

If your site isn't working:

1. Make sure all file paths are relative (starting with `./` not `/`)
2. Check that image paths are correct
3. Verify the `.nojekyll` file exists in the repository root
4. Check the GitHub Pages settings to ensure your site is being deployed from the correct branch

## Making Updates

To update your website:

1. Make changes to the files locally
2. Upload the updated files to GitHub using the same method as before
3. GitHub Pages will automatically redeploy your site with the changes
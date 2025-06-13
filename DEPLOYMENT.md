# Deployment Guide

This guide will help you deploy "The Art of Soccer War" to Netlify via GitHub.

## Files Required for Deployment

Your repository should contain these files (all located in the `/deploy` folder):
- `index.html` - The main website file
- `README.md` - Project documentation
- `netlify.toml` - Netlify configuration
- `.gitignore` - Git ignore rules
- `LICENSE` - Creative Commons Attribution-NonCommercial license
- `DEPLOYMENT.md` - This deployment guide

## Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., "art-of-soccer-war")
5. Make it public (required for free Netlify hosting)
6. Don't initialize with README (we already have one)
7. Click "Create repository"

## Step 2: Upload Files to GitHub

### Option A: Using GitHub Web Interface
1. On your new repository page, click "uploading an existing file"
2. Drag and drop all the files from your `/deploy` project folder
3. Add a commit message like "Initial commit - Art of Soccer War site"
4. Click "Commit changes"

### Option B: Using Git Command Line
```bash
# Navigate to your deploy folder
cd /path/to/your/project/deploy

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit - Art of Soccer War site"

# Add remote origin (replace USERNAME and REPO-NAME)
git remote add origin https://github.com/USERNAME/REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Deploy to Netlify

1. Go to [Netlify.com](https://netlify.com) and sign up/sign in
2. Click "New site from Git"
3. Choose "GitHub" as your Git provider
4. Authorize Netlify to access your GitHub account
5. Select your repository from the list
6. Configure build settings:
   - **Branch to deploy:** `main`
   - **Build command:** (leave empty)
   - **Publish directory:** (leave empty or put `.`)
7. Click "Deploy site"

## Step 4: Configure Custom Domain (Optional)

1. In your Netlify site dashboard, go to "Site settings"
2. Click "Change site name" to customize your subdomain
3. Or add a custom domain under "Domain management"

## Step 5: Enable Automatic Deployments

This is already configured! Every time you push changes to your GitHub repository's main branch, Netlify will automatically rebuild and deploy your site.

## Updating Your Site

To make changes:
1. Edit your files locally in the `/deploy` folder
2. Commit and push changes to GitHub:
   ```bash
   git add .
   git commit -m "Description of your changes"
   git push
   ```
3. Netlify will automatically deploy the updates

## License Information

This project uses the **Creative Commons Attribution-NonCommercial 4.0 International License**:
- ✅ **Free for personal and educational use**
- ✅ **Can be shared and adapted**
- ❌ **No commercial use without permission**
- 📧 **Contact copyright holder for commercial licensing**

## Troubleshooting

### Site Not Loading
- Check the Netlify deploy log for errors
- Ensure `index.html` is in the root directory
- Verify all file paths are correct

### Build Failures
- This is a static site with no build process, so builds should always succeed
- If issues persist, check the `netlify.toml` configuration

### Performance Optimization
- The site is already optimized for fast loading
- Netlify automatically provides CDN and compression
- The `netlify.toml` file includes caching headers

## Support

If you encounter issues:
1. Check Netlify's documentation
2. Review GitHub's help pages
3. Ensure all files are properly committed to your repository

Your site will be available at: `https://your-site-name.netlify.app` 
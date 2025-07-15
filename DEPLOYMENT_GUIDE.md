# Comfort Living Real Estate - Netlify Deployment Guide

## Current Deployment (Manual Upload via GitHub)

### Step 1: Create GitHub Repository
1. Go to [GitHub.com](https://github.com) and sign in
2. Click "New repository"
3. Name it: `comfort-living-real-estate`
4. Make it **Public** (required for free Netlify hosting)
5. Don't initialize with README, .gitignore, or license
6. Click "Create repository"

### Step 2: Upload Files to GitHub
1. Download the `netlify-deployment.tar.gz` file from Replit
2. Extract it to get the `public` folder
3. In your GitHub repository:
   - Click "uploading an existing file"
   - Drag the entire `public` folder contents
   - Also upload: `netlify.toml`, `package.json`, `README.md`
   - Commit with message: "Initial deployment - Comfort Living Real Estate"

### Step 3: Connect to Netlify
1. Go to [Netlify.com](https://netlify.com) and sign up/login
2. Click "New site from Git"
3. Choose "GitHub" and authorize Netlify
4. Select your `comfort-living-real-estate` repository
5. **Build settings:**
   - Build command: `npm run build`
   - Publish directory: `dist/public`
   - Node version: 20
6. Click "Deploy site"

### Step 4: Configure Custom Domain (Optional)
1. In Netlify dashboard → Domain settings
2. Add custom domain: `comfortlivingrealestate.com`
3. Follow DNS configuration instructions
4. Enable HTTPS (automatic)

## Monthly Updates (Current Workflow)

### In Replit:
1. Add new projects to `server/storage.ts`
2. Update property images in `attached_assets/`
3. Run `npm run build`
4. Download `dist/public` folder

### Deploy to Netlify:
1. Go to your GitHub repository
2. Delete old files and upload new `dist/public` contents
3. Netlify will automatically redeploy (takes 2-3 minutes)

## Future Workflow (When Git Lock is Fixed)

### One-Time Setup:
1. In Replit, initialize git:
   ```bash
   git init
   git remote add origin https://github.com/yourusername/comfort-living-real-estate.git
   ```

2. Create `.gitignore`:
   ```
   node_modules/
   dist/
   .env
   .replit
   replit.nix
   ```

3. Push initial code:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push -u origin main
   ```

### Monthly Updates (Future):
1. Make changes in Replit
2. Commit and push:
   ```bash
   git add .
   git commit -m "Added new luxury project: [Project Name]"
   git push
   ```
3. Netlify automatically builds and deploys

## Email Configuration

The contact form uses FormSubmit and requires no setup:
- ✅ Emails sent to: `info@comfortlivingrealestate.com`
- ✅ Professional table format
- ✅ Redirect to thank-you page
- ✅ Spam protection included

## Site Features Ready for Deployment

- ✅ 16 luxury Dubai development projects
- ✅ Professional image galleries for each project
- ✅ Mobile-responsive design
- ✅ Contact form with FormSubmit integration
- ✅ Team profiles (Joe Hardy & Tyrone Herbert)
- ✅ Property filtering by type
- ✅ Individual project detail pages
- ✅ Professional branding and styling

## Troubleshooting

### If site doesn't load:
1. Check build logs in Netlify dashboard
2. Verify publish directory is set to `dist/public`
3. Ensure `netlify.toml` file is in repository root

### If contact form doesn't work:
1. Verify FormSubmit email: `info@comfortlivingrealestate.com`
2. Check redirect URL matches your domain
3. Test form submission on live site

### If images don't display:
1. Verify all images are in `public/attached_assets/`
2. Check image paths in `server/storage.ts`
3. Confirm images were uploaded to GitHub

Your luxury real estate website is now ready for multi-millionaire clients with flawless functionality and professional presentation.
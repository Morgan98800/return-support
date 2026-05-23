# Return iOS App — Support & Privacy Website

This repository contains the official public support website for the iOS app **Return**, a quiet curiosity app designed for saving thoughts, links, and topics you want to explore later.

The website is fully static, uses plain semantic HTML5 and vanilla CSS, carries zero external dependencies or trackers, and is completely pre-configured for instant hosting on **GitHub Pages**.

## Repository Structure

```text
├── index.html            # Landing / Home Page
├── 404.html              # Minimal Not Found Page
├── support/
│   └── index.html        # App Store Connect Support URL (FAQ & Contact)
├── privacy/
│   └── index.html        # App Store Connect Privacy Policy URL (Plain English)
├── assets/
│   └── styles.css        # Unified Design System Stylesheet
├── robots.txt            # Search Spider Directives
├── sitemap.xml           # Search Sitemap
└── README.md             # Setup Guide & Checklist (This File)
```

---

## How to Publish with GitHub Pages

Follow these exact steps to make this support website live and accessible:

1. **Create a GitHub Repository**: 
   - Sign in to GitHub and click **New repository**.
   - Set the Repository Name (e.g., `return-support` or `username.github.io` where `username` is your actual GitHub username).
   - Keep the repository **Public** (required for free GitHub Pages tier).
   - Do *not* initialize it with a README, `.gitignore`, or license (since you will push these local files).

2. **Push These Files to GitHub**:
   - Open your terminal and navigate to this folder.
   - Run the following commands:
     ```bash
     git init
     git add .
     git commit -m "Initial commit: Return support and privacy site"
     git branch -M main
     git remote add origin https://github.com/your-username/your-repo-name.git
     git push -u origin main
     ```

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub.com.
   - Click on the **Settings** tab.
   - In the left-hand menu, under the "Code and automation" section, click on **Pages**.
   - Under **Build and deployment** &rarr; **Source**, make sure **Deploy from a branch** is selected.
   - Under **Branch**, select `main` from the dropdown and set the folder to `/ (root)`.
   - Click **Save**.

4. **Verify the Build**:
   - GitHub will run an automated action to build and deploy your site (usually takes under 1 minute).
   - Once completed, the live URL will be shown at the top of the Settings &rarr; Pages screen.

---

## Expected Live URLs

All links within this site are coded as **relative paths**, which ensures that the website functions perfectly regardless of whether it is hosted at the root domain or a repository subdirectory.

### Option A: Hosted as a Project Repository
If your repository is named `return-support`, the live URLs will be:
- **Home Page**: `https://username.github.io/return-support/`
- **Support URL**: `https://username.github.io/return-support/support/`
- **Privacy Policy URL**: `https://username.github.io/return-support/privacy/`

### Option B: Hosted as your User Site
If your repository is named `username.github.io` (your exact GitHub username), the live URLs will be:
- **Home Page**: `https://username.github.io/`
- **Support URL**: `https://username.github.io/support/`
- **Privacy Policy URL**: `https://username.github.io/privacy/`

---

## Pre-Submission App Store Checklist

Before you submit these URLs to App Store Connect or release your app, complete the following items:

- [ ] **Customize Email Address**:
  - Replace `support@example.com` in:
    - [ ] `index.html` (footer contact mailto link)
    - [ ] `support/index.html` (main support section and footer contact link)
    - [ ] `privacy/index.html` (section 15 contact address and footer link)
- [ ] **Customize Privacy Entity**:
  - Open `privacy/index.html` and search for `[Your legal name or company name]`. Replace it with your actual legal developer name or corporate entity as listed in your Apple Developer account.
- [ ] **Set Dates**:
  - In `privacy/index.html`, replace both `[Insert date]` placeholders in the meta section with the live date (e.g., `May 23, 2026`).
- [ ] **Update Sitemap & Robots URLs**:
  - In `sitemap.xml`, replace `https://username.github.io/return-website` with your actual live URL structure.
  - In `robots.txt`, update the `Sitemap:` path to point to your live site.
- [ ] **Verify Public Reachability**:
  - Open the live URLs in your web browser (including on a mobile device) to verify there are no relative link breaks or CSS stylesheet glitches.
- [ ] **Submit to App Store Connect**:
  - Paste your **Support URL** into the Support URL field under App Store Connect App Information.
  - Paste your **Privacy Policy URL** into the Privacy Policy URL field under App Store Connect App Information.
- [ ] **Add to iOS App Settings**:
  - Integrate these same links into your iOS app's Settings/About screen so they can be accessed natively by users in the app.

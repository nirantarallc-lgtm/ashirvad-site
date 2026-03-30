# Deployment Guide

## 1. Overview

- This project is a static website.
- The site is hosted on GitHub Pages.
- The repository is `https://github.com/nirantarallc-lgtm/nirantara-landing-page`.
- GitHub Pages deploys from the `main` branch root.
- Any push to `main` automatically triggers deployment.
- The production domain is `https://nirantara.online`.

## 2. Local Development Workflow

1. Make changes locally in the project folder:

   `C:\Users\rajee\Documents\1. Business\Nirantara Landing Page`

2. Preview changes in a browser before deploying.

- For simple checks, open the relevant `index.html` file directly in the browser.
- Verify links, layout, and page-specific content before pushing.

## 3. Deploying Changes

Run these commands from the project root:

```powershell
git status
git add .
git commit -m "your message"
git push origin main
```

What this does:

- `git status` shows changed files.
- `git add .` stages your changes.
- `git commit -m "your message"` records the update in git history.
- `git push origin main` pushes the changes to GitHub.
- Once the push completes, GitHub Pages automatically deploys the updated site.

## 4. Verifying Deployment

After pushing to `main`, wait about 1 to 2 minutes for GitHub Pages to finish publishing.

Check these URLs:

- Main site: `https://nirantara.online/`
- Privacy policy: `https://nirantara.online/nourishiq/privacy-policy/`
- Terms of use: `https://nirantara.online/nourishiq/terms-of-use/`
- Delete account: `https://nirantara.online/nourishiq/delete-account/`

If changes do not appear immediately:

- Wait another minute.
- Perform a hard refresh with `Ctrl + Shift + R`.

## 5. Project Structure

GitHub Pages routing for this project depends on folder-based pages.

Rule:

- Each page should live inside its own folder and use an `index.html` file.

Example:

```text
/nourishiq/delete-account/index.html
```

This produces the URL:

```text
https://nirantara.online/nourishiq/delete-account/
```

If a page is not structured this way, the expected clean URL may not work.

## 6. Rules / Best Practices

- Always make edits locally.
- Never edit files directly in the GitHub web UI.
- Never delete or rename the `CNAME` file.
- Always verify the live site after deployment.
- Keep paths consistent with the existing static site structure.

## 7. Troubleshooting

### A. Page not loading

- Check that the page is inside the correct folder.
- Confirm that an `index.html` file exists in that folder.
- Confirm the URL matches the folder path.

### B. Styles not loading

- Check CSS file paths.
- Prefer absolute paths where appropriate, for example:

```text
/nourishiq/legal.css
```

- Confirm the CSS file exists at the expected location.

### C. Changes not visible

- Wait up to 2 minutes after pushing.
- Hard refresh the page with `Ctrl + Shift + R`.
- Confirm your latest commit was pushed to `main`.

### D. Git issues

- Confirm you are on the `main` branch.
- Confirm `git push origin main` completed successfully.
- Run `git status` to make sure there are no unexpected uncommitted changes.

## 8. Optional Future Improvements

- Add GitHub Actions for more controlled deployments.
- Add a pull request based workflow before production deploys.
- Add a staging environment for preview and review before publishing.
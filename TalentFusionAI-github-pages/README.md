# TalentFusionAI — GitHub Pages Edition

This is the **static GitHub Pages version** of TalentFusionAI. It runs entirely in the browser, so GitHub does not need to run Node.js, an API server, or a database.

## Features

- Dashboard and analytics
- Student directory
- Add and edit student records
- Evidence-based AI insight reports
- Weighted and point-based scoring
- Browser persistence using `localStorage`

## Publish with GitHub Pages

### Option A: Upload through GitHub.com

1. Create a new GitHub repository, for example `talentfusionai`.
2. Extract this folder.
3. Upload **all files inside this folder** to the root of the repository.
4. Commit the files.
5. Open the repository’s **Settings → Pages**.
6. Under **Build and deployment**, select:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
7. Click **Save**.
8. After GitHub finishes deploying, open the URL shown on the Pages settings screen.

It will usually look like:

```text
https://YOUR-USERNAME.github.io/REPOSITORY-NAME/
```

### Option B: Upload with Git

From this folder:

```bash
git init
git add .
git commit -m "Add TalentFusionAI GitHub Pages app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Then enable GitHub Pages using the repository settings described above.

## Important: where student edits are stored

Because GitHub Pages is static hosting, student edits are saved in the browser’s **localStorage**. This means:

- Changes remain on the same browser and device.
- Changes are not automatically shared with other users.
- Changes are not committed back to GitHub.
- Clearing browser site data resets the local changes.

For a real multi-user system with shared student records, a backend database/API must be added separately.

## Local test without Node.js

You can test the static version with Python:

```bash
python3 -m http.server 8000
```

Open <http://localhost:8000>.

## Demo access

The interface opens directly as a dashboard demo. If your customized version includes the login screen, use:

```text
Username: admin
Password: cit123
```

## Files

```text
index.html              Main page
app.js                  Browser-only application logic
styles.css              Interface styling
data/students.json       Initial sample records
.nojekyll                Prevents GitHub Pages processing issues
manus-routes.json        Route metadata
```

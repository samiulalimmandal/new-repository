# Academic Collective

A responsive, four-person academic portfolio website built with HTML, CSS and vanilla JavaScript. It is designed for free hosting on GitHub Pages.

## Preview locally
Because the site loads `data/profiles.json` with `fetch()`, open it through a local web server rather than double-clicking `index.html`.

If Python is installed:
```bash
python -m http.server 8000
```
Then visit http://localhost:8000.

## Update your details
All profile information lives in `data/profiles.json`. Open it in GitHub or a text editor and edit the matching person object.

- `name`, `role`, `department`, `institution`, `location`, `email`, `phone`, `bio`
- `interests`, `education`, `experience`, `projects`, `publications`, `skills`
- `social`: paste full profile URLs. Empty values hide that social button.
- `photo`: path to the profile image
- `cv`: path to the PDF CV

Keep JSON syntax valid: use double quotes around keys and text, and commas between items. Do not add a comma after the final item in an array/object.

## Replace a profile photo
1. Upload a JPG, PNG or WebP image to `assets/images/`.
2. Update that person's `photo` value in `data/profiles.json`, for example `"photo": "assets/images/person1.jpg"`.
3. Commit the change. A square image works best. SVG placeholders are included until you add real photos.

## Replace a CV PDF
1. Upload the real CV to `assets/cv/`, for example `person1-cv.pdf`.
2. Keep or update the person's `cv` value in `data/profiles.json`.
3. The profile page has View CV and Download CV links. Replace the included sample PDFs with the real files.

## Add another person
1. Copy one complete person object in `data/profiles.json`.
2. Give the new person a unique `id` such as `person5`.
3. Add their photo and CV under `assets/images/` and `assets/cv/`.
4. Update the `photo` and `cv` paths.
5. Save. The homepage, research filters, and contact page automatically include the new person.

Each profile has a shareable URL such as `profile.html?id=person1`.

## Publish with GitHub Pages
1. Create a new GitHub repository, for example `academic-collective`.
2. Upload all files and folders from this project to the repository root (not inside another nested folder).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then Save.
6. Wait for GitHub Pages to publish. Your site URL will appear on the Pages settings screen.

After any edit, commit the changes to GitHub. GitHub Pages will publish the update automatically.

## Notes
- This is a static site: no database or paid hosting is required.
- Social buttons appear only when a valid URL is supplied.
- The included CV PDFs are clearly marked sample placeholders. Replace them before publishing.
- The site uses Google Fonts from the internet; system fonts remain as fallback.

# VERSE ONE: The Shearer's Gospel
**The Verse Project — Landing Page**

A cinematic single-page landing site for the VERSE ONE animated film project.

---

## Deploying on GitHub Pages

1. Create a new repository on GitHub (e.g. `verse-one` or `theverseprojects`)
2. Push this folder's contents to the `main` branch
3. Go to **Settings → Pages**
4. Under **Source**, select `Deploy from a branch` → `main` → `/ (root)`
5. Save — your site will be live at `https://yourusername.github.io/repo-name`

To use a custom domain (e.g. `theverseprojects.com`):
- Add a `CNAME` file to this folder containing just your domain: `theverseprojects.com`
- Point your domain's DNS to GitHub Pages (see GitHub's docs)

---

## Customising

### Hero Image
The hero currently pulls your image from the WordPress CDN:
```
https://theverseprojects.com/wp-content/uploads/2025/04/The-Verse-Project-Shearer.png
```
To self-host it (recommended for independence from WordPress):
1. Download the image
2. Place it in an `assets/` folder in this repo
3. In `index.html`, find `.hero-img` and change the `background-image` URL to `./assets/your-image.jpg`

### Email Signup
The email form is wired to a placeholder function. To connect it:
- **Mailchimp**: Replace the `handleSignup()` function body with their embedded form POST
- **ConvertKit**: Use their JS embed snippet
- **Brevo (formerly Sendinblue)**: Use their form API
- **Buttondown / Substack**: Direct POST to their subscriber endpoint

The comment in `index.html` marks exactly where to make the change.

### Content Updates
All content lives directly in `index.html` — no build tools, no dependencies. Edit the HTML directly and push to deploy.

---

## Structure

```
verse-one/
├── index.html      ← The entire site (single file, no build required)
├── README.md       ← This file
└── assets/         ← Add your images here (create this folder)
    └── hero.jpg    ← Self-hosted hero image (optional)
```

---

## Tech Stack
- Pure HTML / CSS / JS — no frameworks, no build step
- Google Fonts: Bebas Neue, Playfair Display, DM Sans
- GitHub Pages compatible out of the box

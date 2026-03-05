# Site Management Guide

This site is a static HTML/CSS site hosted on **GitHub Pages** at:

**https://johnoh26.github.io/resume/**

No build tools, no dependencies. Just edit HTML files and push to `main`.

---

## 1. Deploying Changes

1. Edit any HTML file locally
2. Commit and push to the `main` branch:
   ```bash
   git add .
   git commit -m "Your message"
   git push
   ```
3. Wait ~60 seconds, then visit https://johnoh26.github.io/resume/ to see the changes live.

---

## 2. Adding a Project

### Add to `projects.html` (full list)

Open `projects.html` and copy an existing `<div class="card">` block:

```html
<div class="card">
  <h2>Your Project Name</h2>
  <p>One or two sentences describing the project.</p>
  <div class="card-links">
    <a href="https://your-demo-url.com" target="_blank" rel="noopener">Demo</a>
    <a href="https://github.com/johnoh26/your-repo" target="_blank" rel="noopener">Repo</a>
  </div>
</div>
```

Paste it inside the `<div class="project-grid">` section and update the title, description, and links.

### Optionally feature it on `index.html`

Open `index.html`, find the `<section id="projects">`, and add the same card block there (keep to 2–3 featured cards).

---

## 3. Adding a Blog Post

### Step 1 — Create the post file

Copy `blog/2026-03-04-example-post.html` and rename it using the pattern:

```
blog/YYYY-MM-DD-short-title.html
```

For example: `blog/2026-04-15-lessons-from-my-first-job.html`

Update the file:
- Change `<title>` to your post title
- Change `<p class="post-meta">` to the publish date
- Change `<h1>` to your post title
- Replace the body content inside `<div class="post-body">`

### Step 2 — Add it to `blog.html`

Open `blog.html` and add a new `<li>` inside `<ul class="post-list">`:

```html
<li>
  <p class="post-meta">2026-04-15</p>
  <h2><a href="blog/2026-04-15-lessons-from-my-first-job.html">Lessons from My First Job</a></h2>
  <p class="excerpt">A brief one-sentence description of the post.</p>
</li>
```

Also remove or hide the `<p class="empty-state">` paragraph once you have real posts.

### Step 3 — Optionally feature it on `index.html`

Open `index.html`, find `<section id="blog">`, and add the same `<li>` to the list there.

---

## 4. Updating the Resume Link

The resume Google Drive link appears in the nav of every page. Search for the current URL:

```
https://drive.google.com/file/d/1GHyvgiOmTtVBsCVSa7D1Qg2J0_3Vo4Ai/view?usp=drive_link
```

Replace it with your new Google Drive share link in:
- `index.html`
- `projects.html`
- `blog.html`
- `blog/*.html` (any post files)

---

## 5. File Structure Reference

```
resume/
├── index.html                  ← Homepage (hero, skills, featured projects, blog preview)
├── projects.html               ← Full project list
├── blog.html                   ← Blog post listing
├── blog/
│   ├── 2026-03-04-example-post.html   ← Template — copy this for new posts
│   └── YYYY-MM-DD-your-post.html      ← Your actual posts go here
├── howto.md                    ← This file
└── README.md                   ← Project history notes
```

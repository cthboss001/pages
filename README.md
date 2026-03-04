# 🗂️ Projects Showcase — GitHub Pages Portfolio

A clean, dark portfolio page that lists all your deployed GitHub Pages projects in one place. Supports live search and tag filtering. No frameworks, no build step — just edit `index.html` and push.

---

## 🚀 Quick Setup

1. Create a new GitHub repo (e.g. `my-portfolio` or `projects`)
2. Drop `index.html` into the root
3. Go to **Settings → Pages → Source → main branch → / (root)**
4. Your site will be live at `https://yourusername.github.io/my-portfolio`

---

## ✏️ How to Add a New Project

Open `index.html` and find the comment that says:

```html
<!-- ── ADD MORE PROJECTS HERE ── -->
```

Copy one of the existing card blocks and paste it just above that comment. Here's the template:

```html
<a class="card" href="YOUR_GITHUB_PAGES_URL" target="_blank" rel="noopener" data-tags="Tag1,Tag2">
  <div class="card-thumb">
    <div class="thumb-bg" style="background: linear-gradient(135deg, #1a1030 0%, #2a1050 100%);"></div>
    <span class="emoji">🚀</span>
  </div>
  <div class="card-body">
    <div class="card-top">
      <span class="card-title">Project Name</span>
      <span class="card-arrow">↗</span>
    </div>
    <p class="card-desc">One or two sentences about what this project does.</p>
    <div class="card-meta">
      <span class="tag tag-purple">Tag1</span>
      <span class="tag tag-green">Tag2</span>
    </div>
  </div>
</a>
```

### Fields to change

| Field | Where | What to put |
|---|---|---|
| `href="..."` | `<a>` tag | Full URL to your GitHub Pages site |
| `data-tags="..."` | `<a>` tag | Comma-separated tags (used for filter buttons) |
| `<span class="emoji">` | card-thumb | Any emoji that represents the project |
| `thumb-bg` gradient | inline style | Two hex colors for the card background |
| `card-title` | card-body | Project name |
| `card-desc` | card-body | Short description (1–2 sentences) |
| `<span class="tag ...">` | card-meta | Tag labels (must match `data-tags`) |

---

## 🎨 Tag Color Classes

Pick any of these for your `.tag` elements:

| Class | Color |
|---|---|
| `tag-purple` | Purple / violet |
| `tag-pink` | Pink / rose |
| `tag-green` | Mint green |
| `tag-blue` | Sky blue |
| `tag-orange` | Warm orange |

---

## 🎨 Thumb Gradient Ideas

Change the two hex colors in `thumb-bg` for each card to give it a unique tint:

```
Purple vibe:   #1a1030  →  #2a1050
Ocean:         #0d2030  →  #0d3040
Forest:        #0d3020  →  #0d4030
Sunset:        #301510  →  #402010
Crimson:       #301020  →  #401030
```

---

## 📝 Editing Your Name / Tagline

Look for **EDIT SECTION 1** in the file:

```html
<!-- ▶ EDIT SECTION 1: Your name & tagline -->
```

Change the `<h1>` lines and the `<p class="subtitle">` to your own copy.

---

## 📊 Editing the Stats Bar

Look for **EDIT SECTION 2** — the project count is automatic, but you can change the second stat label or add more `stat-item` divs.

---

## 🗑️ Removing a Project

Delete the entire `<a class="card" ...> ... </a>` block for that project. The project count and filter tabs update automatically.

---

## 💡 Tips

- **Tags are auto-generated** — whatever you put in `data-tags` becomes a filter button. No extra setup needed.
- **Project count is automatic** — it reads how many cards exist on the page.
- **Search works instantly** — it searches title, description, and tags.
- The site is fully static — no JavaScript dependencies, no API keys, no build process.

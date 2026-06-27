# Eun Kyoung Choe — academic website (Jekyll)

A tight, responsive academic site. Spectral headings · Source Sans 3 body ·
IBM Plex Mono labels, with a blue primary accent and amber secondary.

All the content you'll change regularly lives in **`_data/*.yml`** and
**`_posts/`** — you rarely need to touch HTML.

## Run locally

```bash
cd jekyll-site
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

## Deploy on GitHub Pages

1. Create a repo. For a personal site, name it `<username>.github.io`
   (then leave `baseurl: ""` in `_config.yml`). For a project repo, set
   `baseurl: "/<repo-name>"`.
2. Push the contents of this `jekyll-site/` folder to the repo root.
3. In the repo: **Settings → Pages → Build and deployment → Source:
   GitHub Actions** (or "Deploy from a branch" → `main` / root).
4. Your site builds automatically on every push.

## Where everything lives

| You want to change… | Edit this |
|---|---|
| Name, tagline, email, office, CV & Scholar links, "last updated" | `_config.yml` |
| Research blurb | `_config.yml` (`research:`) |
| Top navigation | `_data/nav.yml` |
| Research-area bullets | `_data/areas.yml` |
| Travel line under the photo | `_data/travel.yml` |
| Homepage project cards | `_data/projects.yml` |
| News items | `_data/news.yml` |
| Publications | `_data/publications.yml` |
| Courses | `_data/teaching.yml` |
| Students / lab members | `_data/students.yml` |
| Blog posts ("Writing") | add files to `_posts/` |
| Your photo | replace `assets/img/profile.jpeg` |
| Colors, fonts, spacing | `assets/css/style.css` (`:root` variables at top) |

### Notes

- After editing `_config.yml` you must restart `jekyll serve` for changes to show.
- `_data` files are YAML — keep the indentation (2 spaces) and quote any value
  that contains a colon.
- Publications are grouped by `year`; add a new `- year:` block at the top for
  the newest year. `award:` and `links:` are optional per paper.
- Student `photo:` is optional — leave it `""` for a blank avatar circle.
- A new post is a file named `_posts/YYYY-MM-DD-title.md` with the front matter
  shown in the sample post.

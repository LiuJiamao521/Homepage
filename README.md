# Jiamao Liu — Personal Academic Homepage

Personal academic website for **Jiamao Liu** (single-cell & spatial multi-omics, Xiamen University). Served with nginx via docker-compose.

## Pages

| File | Content |
| --- | --- |
| `html/index.html` | Home — intro, photo, elsewhere links, contact |
| `html/research.html` | Research themes + Software & open source |
| `html/publications.html` | Publication timeline |
| `html/activity.html` | Education, skills, posters, awards |
| `html/cv.html` | Inline PDF viewer for `JLiu_s_resume.pdf` |
| `html/style.css` | Single shared stylesheet (design tokens, self-hosted fonts) |

## Run locally / deploy

Requires Docker. The `ssl/` certificate files are **git-ignored** — place your
own `jiamao-liu.com.pem` / `.key` there on the server before starting.

```bash
docker compose up -d
```

Serves on ports 80/443 per `nginx.conf` (the HTTPS block is currently
commented out; uncomment when certificates are present).

## Notes

- Fonts (Inter, Source Serif 4) are self-hosted in `html/fonts/` so the site
  does not depend on Google Fonts.
- To update the resume, replace `html/JLiu_s_resume.pdf` (and optionally the
  same file in this repository's parent GitHub project).
- All static assets (images, favicons) live under `html/`.

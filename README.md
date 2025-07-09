# Is Jenny Sick?

A **tiny, single‑page website** that answers one (very important) question for friends and family:

> **Is Jenny sick?**

You can see it live at [**https://isjennysick.com**](https://isjennysick.com) (or the custom domain you’ve mapped in `CNAME`).

---

## How It Works

- **Static HTML only** – everything lives in `index.html` so you can host it on GitHub Pages or any static host.
- **Manual toggle** – you edit one word (`Yes` / `No`) and one CSS class (`yes` / `no`) when Jenny’s status changes.
- **Timestamp** – an inline JavaScript snippet displays the last updated time. You update the `LAST_UPDATED` string when you flip the status; if you forget, the script falls back to the page’s `document.lastModified` value.
- **Zero dependencies** – no build step, no frameworks.

---

## Updating the Status (🖐 30‑second workflow)

1. Open `index.html`.
2. Change the word inside `<p id="status">` from `No` → `Yes` (or vice‑versa).
3. Change the class from `status no` → `status yes` (or vice‑versa) so the color switches.
4. In the `<script>` block, update the `LAST_UPDATED` string (e.g. `Jul 8 2025 21:45 CDT`).
5. Commit & push – done!

> **Pro tip:** Keep the status flip and timestamp update in the *same commit* so your Git history doubles as a health log.

---

## Recent Revisions (Jul 8 2025)

| Change                     | Details                                                                                                                        |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **🌈 Fresh styling**       | Added inline CSS with the *Nunito* font, soft background, pill‑style status badge, and light drop‑shadow card.                 |
| **⏰ Timestamp script**     | New JS block shows the last update automatically, falling back to `document.lastModified` if you forget to set `LAST_UPDATED`. |
| **Single‑file simplicity** | CSS & JS moved inline so `index.html` is completely self‑contained.                                                            |
| **Color‑coded status**     | Green for `No` (healthy), red for `Yes` (sick).                                                                                |

---

## File Structure

```
/ (repo root)
 ├─ index.html   # The entire site (HTML + CSS + JS)
 ├─ CNAME        # Custom domain for GitHub Pages (optional)
 └─ README.md    # You are here
```

---

## Roadmap / Nice‑to‑Haves

- **GitHub Action** to toggle the status & timestamp via Issue comment or web form.
- **PWA manifest** so family can “install” the site on phones.
- **Emoji mode** – swap text for ✅ / 🤒 icons.
- **Analytics‑light** – maybe Plausible or GoatCounter to track visits.

Got an idea? Open an Issue or PR!

---

## License

MIT — do whatever you like, just don’t blame me if Jenny’s status is out‑of‑date 😄

# is-jenny-sick-website
This is a website I have built to let the world know if my wife is sick, or not.

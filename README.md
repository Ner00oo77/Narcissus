# أسطورة ناركيسوس — بحث تفاعلي في الوهم والهوية

Static interactive presentation featuring an editorial-collage landing page, an archival video player, and a 7-slide interactive deck (including the Ancient Greek morphological text lab).

## Project Structure

```text
myth/
├── index.html                  # Landing page, Story Video Player (#story), About modal
├── slides.html                 # 7-slide interactive presentation (Text Lab + 6 chapters)
├── assets/
│   ├── images/
│   │   ├── landing-bg.jpg      # Archival collage desk background
│   │   └── narcissus-cutout.png
│   ├── slides/
│   │   └── slide_1_card_1.jpg … slide_6_card_5.jpg  (24 slide illustrations)
│   └── video/
│       └── story.mp4           # Story video played in "٠٢ / الأسطورة"
├── _drafts/                    # Archived old drafts & UI mockup (ignored on deploy)
├── .gitignore
├── .vercelignore
├── netlify.toml
└── README.md
```

## Editing Doctor & Student Credits

Open `index.html` and edit the `PROJECT_CREDITS` object near the top of the `<script>` tag to replace the doctor name and the 15 student names across the 5 groups.

## Deployment Notes

This is a 100% static HTML/CSS/JS site — no build step required.

- **Netlify Drop / CLI:** Deploy the `myth/` folder directly (`netlify.toml` is preconfigured).
- **Vercel:** Run `vercel` inside `myth/` (`.vercelignore` excludes `_drafts/`).
- **GitHub Pages:** Push `myth/` to a repository and enable Pages from the root branch.
  - Note: `assets/video/story.mp4` is ~92 MiB (under GitHub's 100 MB limit, though GitHub warns above 50 MB; compressing it with HandBrake/FFmpeg to ~20–30 MB is recommended for faster viewer playback and Cloudflare Pages compatibility).

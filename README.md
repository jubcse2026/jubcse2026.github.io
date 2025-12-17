Yearbook — JU CSE Class of 2026
=================================

This repository hosts a simple static yearbook for the Jadavpur University CSE graduating batch (2026). Profiles are contributed via Pull Requests — each contributor adds their photo and a small JSON profile entry.

How to contribute (step-by-step)
--------------------------------

1. Fork this repository and create a new branch for your profile.
2. Add your portrait image to the `images/` folder. Recommended: square JPG/PNG, ~300–800px on the long edge. Example filename: `images/sourav-kumar.jpg`.
3. Create a JSON file for your profile inside the `students/` folder. Copy the provided template `students/template.json` and save as `students/<your-id>.json` (for example `students/sourav-kumar.json`).
4. Commit your changes and open a Pull Request to this repository. After review the maintainer will merge and your profile will appear on the site automatically.

**Note:** The site automatically discovers all JSON files in the `students/` folder (excluding `template.json`) and displays them. No manual manifest updates are needed.

Student JSON template and fields
--------------------------------

Each student JSON file should have the following fields:

- `id` (string): a short identifier matching your filename (no spaces, lowercase).
- `name` (string): full display name.
- `image` (string): path to your image file, e.g. `images/sourav-kumar.jpg`.
- `quote` (string): one short line about your experience (max ~140 chars recommended).

Example `students/sourav-kumar.json`
```json
{
  "id": "sourav-kumar",
  "name": "Sourav Kumar",
  "image": "images/sourav-kumar.jpg",
  "quote": "Four years of challenges, coffee, and great friends."
}
```

Tips
----
- Keep image filenames unique and include your id.
- If unsure, open a draft PR and ask in the description.

Site preview
------------
After merging, GitHub Pages (or any static server) will serve the site at the repository URL. The homepage automatically discovers and loads all JSON files in the `students/` folder (excluding `template.json`) and renders the tiles.

Privacy / content
-----------------
Only include content you're comfortable publishing. By opening a PR you confirm you have the rights to the image you upload.

Maintainer notes
----------------
- Profiles are displayed in the order returned by the GitHub API (typically alphabetical by filename).
- Optionally compress uploaded images for faster load times.

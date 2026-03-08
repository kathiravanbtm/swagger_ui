# Swagger UI GitHub Pages

This repository hosts a static Swagger UI for the `openapi.json` specification. It can be published using GitHub Pages so that the UI is accessible from `https://<your‑username>.github.io/<repo-name>`.

## Setup

1. **Commit the files**
   ```bash
   git init                 # if you haven't already
   git add index.html openapi.json README.md
   git commit -m "Add Swagger UI and OpenAPI spec"
   ```

2. **Push to GitHub**
   Create a repository on GitHub (for example, `codeethnics-api-docs`) and push your local branch:
   ```bash
   git remote add origin git@github.com:<your-user>/<repo-name>.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to the repository on GitHub.
   - Navigate to **Settings** ▶️ **Pages** (or **Settings** ▶ **Code and automation** ▶ **Pages**).
   - Under **Source**, select the branch (`main` or `gh-pages`) and folder (`/ (root)` or `docs/`).
   - Save; GitHub will provide the published URL.

   Alternatively, you can publish from a `gh-pages` branch by building into that branch or using the `gh` CLI:
   ```bash
   git checkout --orphan gh-pages
   git reset --hard
   git add index.html openapi.json
   git commit -m "Publish Swagger UI"
   git push -u origin gh-pages
   ```

4. **Access the UI**
   Visit the URL shown in GitHub Pages settings (e.g. `https://<your-user>.github.io/<repo-name>/`). The Swagger UI should load and display the `openapi.json` specification.

## Customization
- To change the spec URL, edit the `url` option in `index.html`.
- You can add additional styling or configuration options using the [Swagger UI options](https://swagger.io/docs/open-source-tools/swagger-ui/usage/configuration/).

## Notes
- If you put the files in a `docs/` folder instead of root, update the `url` path accordingly (e.g. `docs/openapi.json`).
- GitHub Pages serves static files; the OpenAPI JSON must be publicly accessible.

---

Feel free to fork this repo or modify it to include your own branding and settings.
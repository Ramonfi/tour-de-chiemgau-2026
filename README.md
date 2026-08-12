# Tour de Chiemgau 2026

Static trip-planning page for the Tour de Chiemgau on 15-16 August 2026. The site has no build step or runtime dependencies and can be deployed directly with GitHub Pages.

## Project structure

```text
.
|-- assets/
|   `-- images/       # Local timetable screenshots
|-- .gitignore
|-- index.html        # Complete website: HTML, CSS, and JavaScript
`-- README.md
```

## Local preview

From the repository root, start a local web server:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

Opening `index.html` directly also works, but a local server more closely matches GitHub Pages and avoids browser restrictions associated with `file://` URLs.

## Deploy with GitHub Pages

1. Push the repository to GitHub, with `index.html` in the repository root.
2. Open the repository on GitHub.
3. Go to **Settings > Pages**.
4. Under **Build and deployment**, select **Deploy from a branch** as the source.
5. Select the `main` branch and the `/(root)` folder, then click **Save**.
6. Wait for the Pages deployment to finish. Its status appears in the repository's **Deployments** section.

The site will be available at:

<https://ramonfi.github.io/tour-de-chiemgau-2026/>

Subsequent pushes to `main` automatically redeploy the page.

## Updating the site

- Edit layout, styling, behavior, and page content in `index.html`.
- Store local images in `assets/images/` and reference them with relative paths such as `assets/images/example.png`.
- Keep file and directory names lowercase and avoid spaces so URLs remain predictable.
- Preview changes locally before pushing them to `main`.

## Technical notes

- Fonts are embedded in `index.html`, so no font hosting is required.
- Route maps and the accommodation map are third-party embeds and require an internet connection.
- Pack-list progress is stored only in the visitor's browser via `localStorage`.

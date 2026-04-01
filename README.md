# Thesis Word Budget

Interactive tool for planning word distribution across thesis sections.

## Features

- **Draggable vertical bar** — redistribute words between main sections
- **Subsections** — add, rename, reorder (▲▼), and remove subsections within any section
- **Horizontal sub-bars** — drag to redistribute words within a section
- **Presets** — quick distributions (Equal, Lit-Heavy, Results-Heavy, Balanced)
- **JSON editor** — open/edit/apply configuration as JSON for portability
- **Adjustable total** — 8k–14k word range with page estimates (~525 words/page for 12pt A4)

## Deploy with GitHub Pages

1. Create a new repository on GitHub
2. Upload `index.html` (or push this folder)
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch**, select `main` / `root`
5. Your tool will be live at `https://<username>.github.io/<repo-name>/`

## Usage

- Drag the dividers on the left bar to adjust section proportions
- Click **+** to add subsections, click names to rename them
- Use **▲▼** arrows to reorder subsections
- Click **{ } JSON** to open the config editor — paste saved configs to restore state
- Adjust the total word count slider at the top

## Configuration

Export your distribution via the JSON panel and save it. Paste it back in to restore. The JSON schema:

```json
{
  "total": 11000,
  "sections": [
    {
      "id": "intro",
      "label": "Introduction",
      "color": "#FF91AF",
      "weight": 0.08,
      "subs": [
        { "id": "i1", "label": "Subsection Name", "weight": 0.5 }
      ]
    }
  ]
}
```

## License

MIT

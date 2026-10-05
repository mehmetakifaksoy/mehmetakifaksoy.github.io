# Mehmet Akif Aksoy — Personal AI Security Website

A static Turkish portfolio and technical blog published with GitHub Pages.

## Structure

- `content/articles.json`: editable article titles, summaries, HTML bodies, references and legacy URLs.
- `content/simulation.html`: source of the interactive prompt injection experiment.
- `scripts/build.py`: dependency-free Python site generator.
- `assets/`: shared styles, favicon and editorial cover.
- `yazilar/`, `projeler/`, `hakkimda/`: generated pages.
- `2021/`: redirects preserving original article links.

## Edit and preview

1. Update article data or templates in `scripts/build.py`.
2. Run `python scripts/build.py`.
3. Run `python -m http.server 8765 --bind 127.0.0.1`.
4. Open http://127.0.0.1:8765 and check desktop and mobile layouts.
5. Commit both source files and generated output. Push to `master` to publish.

To add an article, append an object matching the existing schema in `content/articles.json`. Set `published`, `updated` and `note` explicitly for new articles; omit `legacy` when no old URL needs a redirect. Bodies are trusted author-written HTML, never visitor input.

## Content policy

The author profile reflects documented learning projects, without invented qualifications or employment claims. Legacy networking notes were rewritten on October 5, 2026; old URLs remain usable. The original versions remain in Git history.

The simulation replays recorded lab scores and answers. It does not call an LLM, and it does not invent answers when the selected context changes. Citation labels and similarity scores do not establish factual correctness or security. The synthetic injection fixture is educational test data.

Lab source: https://github.com/mehmetakifaksoy/ai-security-fundamentals-lab

## Deployment

GitHub Pages serves committed static files from the root of `master`. `.nojekyll` bypasses Jekyll processing. No runtime dependency, external font or analytics service is required.

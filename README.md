# Maven documentation (Zensical)

Static docs for Maven, built with [Zensical](https://zensical.org/).

## Setup

1. Python 3.14+ (or match your environment).
2. Create a virtualenv and install Zensical:

```sh
python3 -m venv .venv
source .venv/bin/activate
pip install zensical
```

## Run locally

```sh
source .venv/bin/activate
zensical serve -f zensical.toml
```

Open the URL Zensical prints (usually `http://127.0.0.1:8000`).

## Build

```sh
source .venv/bin/activate
zensical build --clean -f zensical.toml
```

Output is written to `site/`.

## Project layout

- `zensical.toml` — site name, nav, theme, repo link.
- `docs/` — Markdown sources.

## GitHub Pages

In the repo **Settings → Pages**, set the source to **Deploy from a branch** and choose **`gh-pages`** (root). The workflow publishes production to the site root and PR previews to `pr/<number>/`.

# Listicle Swipe File

Full-page clones of listicles for reference when writing new listicles for clients. Mirrors the [advertorial-swipes](https://github.com/primalconversions/advertorial-swipes) setup.

**Live site (once swipes are added):** https://primalconversions.github.io/listicle-swipes/

## Status

Empty scaffold — drop URLs into `urls.txt` and run the clone script.

## Adding swipes

```bash
# 1. Add one URL per line to urls.txt
# 2. Clone all of them as self-contained HTML (images embedded)
python3 clone.py

# 3. Rebuild README with view/raw/source links
python3 build_readme.py

# 4. Push
git add -A && git commit -m "Add N listicle clones" && git push
```

Each folder under `swipes/` will contain:
- `index.html` — self-contained page (HTML + CSS + images embedded via `monolith`)
- `source.txt` — original URL

## Requirements

```bash
brew install monolith
```

## How to use the swipes

Click the **view** link in the index to open the rendered listicle, or paste the raw `index.html` content into a Claude conversation when drafting a new listicle — the AI can reference hook structure, item ordering, proof, transitions, and CTAs.

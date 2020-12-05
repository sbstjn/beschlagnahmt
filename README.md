# [beschlagnahmt.org](https://beschlagnahmt.org) ![Jekyll site CI](https://github.com/beschlagnahmt-org/website/workflows/Jekyll%20site%20CI/badge.svg)

Die Webseite wird mittels [Jekyll](https://jekyllrb.com/) generiert.

## Lokale Entwicklung

```bash
# Abhängigkeiten installieren
$ > bundle install

# Jekyll starten
$ > bundle exec jekyll serve
```

## Content

- `_posts` enthält die einzelnen Themen
- `_pages` enthält sonstige Unterseiten

## PDF Export

```bash
$ > pandoc -s -f markdown _pages/about.md _posts/* \
    -o acab.pdf \
    --resource-path=assets \
    --pdf-engine=xelatex \
    --template=.pandoc/template.latex \
    --lua-filter=.pandoc/ remove-toc.lua
```

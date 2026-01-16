# Portfolio Website - Lukas Hügle

Professionelle Portfolio-Website erstellt mit Hugo und dem hugo-coder Theme.

## Technologie-Stack

- **Hugo** (v0.154.5+extended) - Static Site Generator
- **hugo-coder** - Minimalistisches, professionelles Theme
- **GitHub Pages** - Hosting & Deployment
- **GitHub Actions** - Automatisches Deployment

## Features

- Professionelles, minimalistisches Design
- Responsive & Mobile-optimiert
- Blog-Funktionalität mit Taxonomien (Tags, Kategorien, Autoren, Series)
- Deutsche Lokalisierung
- SEO-optimiert
- RSS Feed
- Automatisches Deployment

## Struktur

```
portfolio-website/
├── .github/workflows/
│   └── hugo.yml              # GitHub Actions Deployment
├── archetypes/
│   └── posts.md              # Template für Blog-Posts
├── content/
│   ├── _index.md             # Homepage
│   ├── about.md              # Über mich
│   ├── journey.md            # Werdegang
│   ├── publications.md       # Publikationen & Vorträge
│   └── posts/                # Blog-Posts
│       ├── _index.md
│       └── ai-first.md
├── static/
│   └── images/
│       └── lukashuegle.jpg   # Profilbild
├── themes/
│   └── hugo-coder/           # Hugo Theme
├── hugo.toml                 # Hauptkonfiguration
└── README.md
```

## Lokale Entwicklung

### Voraussetzungen

- Hugo (extended version) installiert
- Git

### Server starten

```bash
cd portfolio-website
hugo server
```

Die Website ist dann unter `http://localhost:1313` erreichbar.

## Content Management

### Seiten bearbeiten

Seiten befinden sich in `content/`:
- `_index.md` - Homepage
- `about.md` - Über mich Seite
- `journey.md` - Werdegang
- `publications.md` - Publikationen & Vorträge

### Blog-Post erstellen

```bash
hugo new posts/mein-post.md
```

Post-Frontmatter-Beispiel:
```toml
+++
draft = false
date = 2026-01-12T12:00:00+01:00
title = "Titel des Posts"
description = "Kurze Beschreibung"
slug = "url-slug"
authors = ["Lukas Hügle"]
tags = ["Tag1", "Tag2"]
categories = ["Kategorie1"]
series = []
+++
```

### Konfiguration

Hauptkonfiguration in `hugo.toml`:
- Persönliche Informationen (`params.author`, `params.info`)
- Social Links (`params.social`)
- Navigation Menu (`languages.de.menu.main`)
- Taxonomien (`taxonomies`)

## Deployment

### Automatisches Deployment

Die Website wird automatisch über GitHub Actions deployed bei jedem Push zum `main`-Branch.

Workflow: `.github/workflows/hugo.yml`

### Manuelle Builds

```bash
hugo --minify
```

Build-Output landet in `public/` (wird nicht in Git committed).

## Theme Anpassungen

Das hugo-coder Theme bietet folgende Anpassungsmöglichkeiten:

- **Color Scheme**: `colorScheme = "auto"` in `hugo.toml` (auto, light, dark)
- **Date Format**: `dateFormat` in `hugo.toml`
- **Avatar**: `avatarURL = "images/lukashuegle.jpg"`
- **Footer**: `footercontent` in `hugo.toml`

## Nützliche Befehle

```bash
# Entwicklungsserver starten
hugo server

# Entwicklungsserver mit Drafts
hugo server -D

# Production Build
hugo --minify

# Neuen Post erstellen
hugo new posts/titel.md
```

## Links & Dokumentation

- [Hugo Dokumentation](https://gohugo.io/documentation/)
- [hugo-coder Theme](https://github.com/luizdepra/hugo-coder)
- [GitHub Pages Dokumentation](https://docs.github.com/en/pages)

## Lizenz

Diese Website nutzt Hugo (Apache 2.0) und hugo-coder Theme (MIT).

# GovCircle Website AI Development Guide

This guide helps AI agents understand and work effectively with the GovCircle website codebase.

## Project Overview

GovCircle is a documentation and governance platform built using:
- Hugo static site generator
- Lotus Docs theme
- Bootstrap SCSS
- Markdown content

## Key Architecture Components

### 1. Content Structure
- `/content/docs/` - Main documentation content in Markdown
- `/content/_index.md` - Landing page content
- Content follows Hugo's hierarchical structure with `_index.md` files

### 2. Theme and Layout
- Based on Lotus Docs theme (imported via Hugo modules)
- Custom layouts in `/layouts/`
- Partial templates in `/layouts/partials/`
- Shortcodes in `/layouts/shortcodes/`

### 3. Asset Management
- Static assets in `/static/`
- Processed assets in `/assets/`
- Generated resources in `/resources/_gen/`

## Development Workflows

### Local Development
1. Install Hugo extended version
2. Run `hugo server` for local development
3. Access site at `http://localhost:1313`

### Content Updates
- Markdown files in `/content/` directory
- Front matter in YAML format
- Support for shortcodes and HTML

### Theme Customization
- Override theme files in `/layouts/`
- Custom SCSS in `/assets/scss/`
- Configure theme in `hugo.toml`

## Project-Specific Conventions

### Front Matter
```yaml
---
title: "Page Title"
description: "Page description for SEO and social sharing"
weight: 10  # Controls ordering in navigation
---
```

### Social Media Integration
- Meta tags configured in `/layouts/partials/head/`
- Social sharing parameters in `hugo.toml`

### Documentation Structure
- Use nested `_index.md` files for section organization
- Maintain consistent heading hierarchy (h1 -> h2 -> h3)
- Place images in `/static/images/` with descriptive names

## Key Configuration Files
- `hugo.toml` - Main configuration file
- `/layouts/index.html` - Homepage template
- `/layouts/partials/head.html` - Document head and meta tags
- `/layouts/partials/docs/` - Documentation-specific templates
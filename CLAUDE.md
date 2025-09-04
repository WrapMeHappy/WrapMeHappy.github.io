# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages site using the Minimal Mistakes theme. The site is configured for Korean content (ko-KR locale) with the title "WrapMeHappy" and serves as a personal blog/portfolio.

## Architecture

### Core Structure
- **Jekyll Theme**: Based on Minimal Mistakes v4.27.3, using gem-based installation
- **Content Organization**: 
  - `_posts/` - Blog posts in Markdown with YAML frontmatter
  - `_pages/` - Static pages (404, category/tag archives)
  - `_data/` - Site navigation and UI text data
  - `_includes/` - Reusable HTML components and analytics
  - `_layouts/` - Page templates (single, archive, home, etc.)
  - `_sass/` - Theme stylesheets and customizations
  - `assets/` - CSS, JavaScript, and images

### Key Features Enabled
- MathJax support for LaTeX equations (enabled site-wide)
- Disqus comments with shortname "wrapmehappy"
- Google Analytics (G-PEDW4ZL4KJ)
- Search functionality with Lunr
- Table of contents (sticky, Korean labels)
- Breadcrumb navigation

## Development Commands

### Preview & Development
```bash
# Start development server with live reload
bundle exec rake preview

# Install dependencies
bundle install

# Build Jekyll site
bundle exec jekyll build

# Serve locally (alternative)
bundle exec jekyll serve
```

### Asset Management
```bash
# Minify JavaScript assets
bundle exec rake js

# Generate copyright notices
bundle exec rake copyright

# Update version numbers across files
bundle exec rake version

# Run all build tasks
bundle exec rake
```

### Testing
The theme includes a test site in `/test/` directory that can be previewed with `bundle exec rake preview`.

## Configuration

### Site Configuration (`_config.yml`)
- Locale set to Korean (ko-KR) with Seoul timezone
- MathJax enabled for mathematical expressions
- Custom author profile with Korean bio
- Google Analytics tracking enabled
- Disqus comments configured

### Content Defaults
- Posts: Single layout with ToC, MathJax, comments enabled
- Pages: Single layout with author profile and MathJax
- Korean UI text for ToC labels ("목차")

## File Structure Notes

- Main site content in root directory
- Demo content exists in `/docs/` (ignored by main site)
- Test content in `/test/` for development
- Theme assets managed via gem, not directly in repository
- Custom images in `/img/` (includes kimbap.png avatar)

## Custom Modifications

The site has been customized from the default Minimal Mistakes theme:
- Korean language configuration and UI text
- Custom author profile and bio
- MathJax support enabled globally
- Specific Google Analytics and Disqus integration
- Custom copyright settings and footer links
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static GitHub Pages site for DataCompound, a data & AI consulting practice. There is no build step, package manager, or test suite — the site is a single `index.html` with all CSS inlined in a `<style>` block, plus two images.

## Deployment

The `main` branch is the live GitHub Pages branch. The working branch is `souzad`. Changes are merged to `main` via pull request to publish. The custom domain is configured via `CNAME`.

## Architecture

- `index.html` — entire site: HTML structure + all CSS in one `<style>` block. No external CSS files, no JavaScript framework, no bundler.
- `images/` — `datacompound-logo.png` (navbar logo) and `datacompound-banner.png` (hero background).
- CSS uses CSS custom properties (`--bg`, `--primary`, `--accent`, etc.) defined in `:root` for theming.
- The hero section uses a CSS-only orbit/chip animation (`@keyframes float1/2/3`).
- Layout is responsive via a single `@media (max-width: 860px)` breakpoint.

## Working in this repo

To preview locally, open `index.html` directly in a browser — no server needed. Changes to `index.html` are immediately visible on reload.

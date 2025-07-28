# Copilot Instructions for jsFiddleGithubDemo

## Project Overview
This repository demonstrates how to use jsFiddle with GitHub-hosted files, focusing on AJAX (Request.HTML) integration and external JS loading. It is a static, front-end only project with no build or test automation.

## Key Components
- `Demo/` — Main jsFiddle demo files:
  - `demo.html` — Entry point for the demo UI.
  - `demo.js` — Uses MooTools `Request.HTML` to fetch HTML from GitHub and update the DOM.
  - `demo.response.html` — Example HTML response loaded via AJAX.
  - `demo.details` — Metadata and documentation for the demo.
  - `demo.css` — Demo-specific styles (uses SCSS-like variables, but no build step).
- `External-JS-In-Request.HTML/` — Shows loading and executing external JS from GitHub:
  - `external.js` — JS file loaded via `<script>` tag in `demo.response.html`.
  - `demo.response.html` — HTML that loads and uses the external JS.

## Patterns & Conventions
- **AJAX Loading:**
  - Uses MooTools `Request.HTML` to fetch and inject HTML from GitHub.
  - Example: `new Request.HTML({ url, update, onSuccess }).send();` in `Demo/demo.js`.
- **External JS:**
  - Loads JS directly from GitHub using a `<script src=...>` tag.
  - Example: See `<script>` tag in `External-JS-In-Request.HTML/demo.response.html`.
- **No Build/Deploy Steps:**
  - All files are static. No npm, node, or build tools are used.
  - CSS uses SCSS-like variables, but is written as plain CSS.
- **No Automated Tests:**
  - There are no test files or test runners. All testing is manual via browser.

## Developer Workflow
- Edit files directly in the `Demo/` or `External-JS-In-Request.HTML/` folders.
- Open `demo.html` or `demo.response.html` in a browser to view changes.
- For AJAX demos, ensure GitHub raw URLs are accessible (CORS may apply).

## Integration Points
- **MooTools** is assumed to be available in the jsFiddle environment (not included in this repo).
- **GitHub Raw URLs** are used for loading both HTML and JS.

## Examples
- To update the AJAX-loaded content, edit `Demo/demo.response.html`.
- To change the external JS logic, edit `External-JS-In-Request.HTML/external.js`.

## References
- See `Demo/demo.js` and `External-JS-In-Request.HTML/demo.response.html` for the main integration patterns.

---
If you add new demos or patterns, update this file to document them for future AI agents and developers.

# HomeBay — Technical Design (Prototype)

## Current architecture

Browser → `index.html` → `styles.css` for layout and responsive design → `app.js` for local filtering, favourites, detail display, and demo interactions.

## Data flow

1. The browser loads the static page.
2. `app.js` loads a small hard-coded set of fictional sample properties.
3. Search and filter inputs run client-side filtering.
4. Listing actions are demo-only; there are no server requests or persistent storage.

## Proposed future architecture

- Front end: React or accessible HTML/CSS/JavaScript
- API: Python Flask or Node.js
- Database: Firebase or MySQL
- Maps: OpenStreetMap or Google Maps, subject to provider terms
- Security: input validation, minimal personal-data collection, access controls, secure transport, abuse reporting, and documented retention policies

## Key risks and mitigations

- Fake/outdated listings: freshness timestamps, report flow, owner verification and manual review.
- Privacy: collect only necessary information and document how it is used.
- Misleading sample data: label demo data clearly and do not imply verification.
- Accessibility: test keyboard navigation, contrast and mobile layouts.

This document describes a prototype and proposed future design, not a production deployment.

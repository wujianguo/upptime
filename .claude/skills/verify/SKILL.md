---
name: verify
description: Verify Upptime site configuration changes against the live endpoint.
---

# Verify Upptime monitoring changes

1. Inspect the `.upptimerc.yml` diff and identify the added or changed site.
2. Parse `.upptimerc.yml` with Python and PyYAML to confirm the site entry is valid YAML.
3. Request the configured URL with redirects enabled and a 30-second timeout.
4. Capture the HTTP status, final URL, content type, and HTML title.
5. Probe a clearly nonexistent path to distinguish a healthy application response from a catch-all success page.

Do not run the generated Upptime workflows locally; their runtime surface is GitHub Actions. Never print secret-backed site headers or URLs.

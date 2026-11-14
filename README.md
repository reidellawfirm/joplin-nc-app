# Joplin for Nextcloud

**Version:** 1.5.1
**Author:** Schuyler "Rocky" Reidel, Reidel Law Firm <schuyler@reidellawfirm.com>
**License:** GPL-3.0-or-later
**Requires:** Nextcloud 28+ · PHP 8.1+

Browse, read and search your Joplin notes inside Nextcloud, as a native app with its own header navigation entry.

Joplin clients already sync their notes to a folder in Nextcloud. This app reads that folder and presents it as a proper notebook/note browser in the web UI — no separate export or sync step.

## Features

- **Native app** — its own entry in the Nextcloud header
- **Notebook and note listing** from your existing Joplin sync folder
- **Human-readable titles** instead of GUID filenames
- **Markdown rendering** in a read-only viewer
- **Full-text search** across titles and note bodies
- **Notebook hierarchy** reconstructed from Joplin's `parent_id` metadata
- **Hides internal metadata** from the UI
- **Index caching** for fast repeated browsing
- **Strictly read-only** — never modifies, renames or rewrites any Joplin file

This app is independent of **Joplin File Titles**; both can be enabled at the same time.

## Installation

```bash
cd /path/to/nextcloud/custom_apps
tar -xzf joplin_nc_app-1.5.1.tar.gz
sudo -u www-data php occ app:enable joplin_nc_app
```

## Configuration

Open **Administration settings → Joplin** and select the folder in Nextcloud Files where your Joplin clients sync (the folder containing `info.json`).

## Usage

1. Click **Joplin** in the Nextcloud header
2. Pick a notebook on the left
3. Select a note to read it
4. Use the search box to search across all notes

## License

GPL-3.0-or-later. See [LICENSE](LICENSE).

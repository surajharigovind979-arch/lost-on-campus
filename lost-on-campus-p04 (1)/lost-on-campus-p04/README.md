# Lost on a 600-Acre Campus

A QR-based gadget recovery prototype for a large university campus. Students who lose a phone, power bank or earbuds can register the item at a Gate Tag Desk, attach a QR sticker, and let finders return it to a nearby Drop Point. Owners claim items by verifying a secret detail.

Team P04 · Lovely Professional University

## Features

- **Desk:** Register a lost gadget, choose a preferred Drop Point (or leave it on auto), generate a QR sticker with a new emoji each time, and print it.
- **Finder:** Look up a sticker code, see the Drop Point on a campus map and change it to where the finder can leave the item, and report found items that have no sticker.
- **Claim:** Verify ownership with the gadget ID and secret detail, and view alerts for items waiting for collection.
- **Register:** Searchable records with masked phone numbers, an activity log, found-item reports, CSV export, and demo data.

## Language

The interface supports English and Hindi (हिन्दी). Use the language selector in the top bar. The choice is saved in the browser. Sticker codes stay in English so that every scanner can read them.

## Privacy

The QR code contains only the gadget ID, gadget type and Drop Point. Owner names and phone numbers are never encoded in the sticker, phone numbers are masked in the admin view, and CSV export excludes names.

## Run locally

No build step is needed. Open `index.html` in any modern browser, or use the VS Code Live Server extension.

The QR code library loads from a CDN, so an internet connection is needed for the QR image. Without it, the sticker code is still shown as text.

## Limitations

This is a prototype.

- Data is stored in the browser's `localStorage` and is not shared between devices.
- There is no authentication for the desk or register views.
- The finder accepts typed or pasted codes, not a live camera scan.
- The secret detail is not encrypted.

## Project structure

```
index.html   # Full application (HTML, CSS and JavaScript in one file)
README.md    # This file
```

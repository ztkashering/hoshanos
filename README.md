# Hoshanos Pre-Order

A single free web page for taking pre-orders for Hoshanos (Aravos bundles) for Hoshana Rabba.
Orders are collected with a free Google Form, which automatically logs every submission into a
Google Sheet you can sort, filter, and export &mdash; no backend, no database, no cost.

## One-time setup (about 5 minutes)

### 1. Create the Google Form

1. Go to [forms.google.com](https://forms.google.com) and click **+ Blank form**.
2. Title it something like "Hoshanos Pre-Order".
3. Add these questions (all as **Short answer** unless noted):
   - **Name** (required)
   - **Phone number** (required)
   - **Email** (optional)
   - **How many sets?** &mdash; make this **Multiple choice** or **Dropdown** with options like 1, 2, 3, 4, 5+ (required)
   - **Pickup or delivery?** &mdash; **Multiple choice**: Pickup / Delivery
   - **Notes / special requests** &mdash; Short answer, optional, "Paragraph" type
4. Click the **Responses** tab, then the green Sheets icon to link a Google Sheet. Every
   submission will now land there automatically, in real time.

### 2. Get the embed link and plug it into the page

1. In the Form editor, click **Send** (top right).
2. Click the **`<>`** (embed) icon.
3. Copy the URL inside `src="..."` from the box shown &mdash; it looks like
   `https://docs.google.com/forms/d/e/XXXXXXX/viewform?embedded=true`.
4. Open `index.html` in this repo and replace **both** occurrences of
   `YOUR_GOOGLE_FORM_EMBED_URL` with that link.

### 3. Fill in your real details

Still in `index.html`, find the block marked `EDIT ME` near the top of the page body and update:
- **Price** per set
- **Pickup Location**
- **Order By** date
- **Set Includes** (how many branches per set, if different from 5)

### 4. Turn on free hosting (GitHub Pages)

1. On GitHub, go to this repo's **Settings → Pages**.
2. Under "Build and deployment", set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Save. GitHub gives you a free URL like `https://ztkashering.github.io/hoshanos/` within a minute or two.
4. Share that link anywhere &mdash; text, WhatsApp, shul group chat, flyer QR code.

## Tracking orders

Every submission appears instantly as a new row in the linked Google Sheet (Responses tab →
Sheets icon). You can sort by name, filter by pickup date, total up quantities with a simple
`SUM` formula, and export to Excel/CSV whenever you want &mdash; no login system or extra
software needed.

## Making changes later

This is a single static file (`index.html`). To change wording, price, or the pickup date,
edit the file directly on GitHub (pencil icon on the file page) and commit &mdash; the live
site updates within a minute.

# The Genealogy Machine: The Making of Social Studies

An expandable, source-attributed research archive for GitHub Pages. No build system, login, database, or API key required.

## Publish

1. Create a GitHub repository, e.g. `genealogy-machine`.
2. Upload `index.html`, `style.css`, `app.js`, `.nojekyll`, and the entire `data/` folder to the repository root. `build.py` is optional and should not be rerun after editing the JSON data: it regenerates the starter dataset.
3. Under **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
4. Open the Pages URL shown in Settings → Pages. For local preview, run `python3 -m http.server 8000` from the folder and visit `http://localhost:8000`.

## Extend the archive

- **Add a bibliographic source:** append a unique `{id,citation,url,access}` object to `data/sources.json`.
- **Add a layer:** use the in-site **Add a layer** form to download a draft, verify it, give it a permanent ID and number, then append it to `data/layers.json`. The form does not write to GitHub directly.
- **Add a relationship:** append `{from,to,label,sourceIds}` to `data/connections.json`.
- **Never publish a layer without sourceIds and a locator.** Include precise pages, archival collection identifiers, or stable document URLs. If the link is only a publisher landing page, retain a precise locator in the layer.
- **Keep claims and questions distinct.** Existing layers are research questions and are explicitly marked provisional. To add a historical factual claim, create a separate evidence record with quotation/paraphrase, pinpoint, and source type before marking verified.

## Citation and editorial caveats

This initial edition reconstructs the **100-layer research inventory** from a conversation. Layers 28–100 have source-level citations and, where known, chapter/page locators. **Layers 1–27 are legacy placeholders**: the earlier conversation does not preserve complete source-to-layer mappings, so they are explicitly marked as needing citation reconciliation. They must not be presented as verified historical findings. Some later layer locators are chapter-level and should be refined to pinpoint pages as research continues. All layer descriptions are interpretive questions, not factual assertions proved by the source.

The archive does **not** include the copyrighted uploaded PDF chapters. Bibliographic attribution and public publisher/DOI links are provided where known. Washington's 2019 standards are included as a bibliographic source record but a complete standards-by-standard data extraction is a separate research phase.

## Recommended next schema expansion

Add `data/evidence.json` records `{id,sourceId,locator,excerptOrParaphrase,sourceType,confidence,editorialNote}` and reference their IDs from layers. This would support document-level verification, competing interpretations, and archival provenance without treating every question as a finding.

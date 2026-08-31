# NLP & Generative AI: Interactive Activities

Companion demos for the *From Words to Worlds* flipbook. Open `index.html` to browse all of them from one page.

## What's in this folder

| File | What it does | Needs internet on first open? |
|---|---|---|
| `index.html` | Hub page linking to everything below | No |
| `nlp_human_language_sort_activity_challenge.html` | Slide 20 technologies into "uses human language" / "does not need language" | No |
| `which-requires-nlp.html` | Shorter 11-item click-to-sort version, good as a later reinforcement check | No |
| `nlp-toolbox-match.html` | Match each NLP task to the real technology that performs it | No |
| `history-eras-activity.html` | Judge what each era of NLP could and couldn't do, era by era | No |
| `search-engine-nlp-lab.html` | Simulated search pipeline: predict a query's meaning, then reveal tokens, interpretation, and region-sensitive results | No |
| `tokenization-demo.html` | Real GPT-2 tokenizer, runs in the browser | **Yes**, first load only |
| `Word_Embeddings_in_3D__What__Meaning__Looks_Like_to_a_Model.html` | Rotatable 3D map of real word embeddings | **Yes**, first load only |
| `Unit_3__Break_a_Real_NLP_Model.html` | Real sentiment classifier, stress-tested with sarcasm and slang | **Yes**, first load only |

The three "Yes" demos download a real AI model from Hugging Face the first time they're opened (a few megabytes). After that first download, the browser caches it and they work offline.

**Not included:** none currently missing — all files listed above should be present in this folder.

## Testing locally

The three demos that download a model **will not work** if opened directly as a `file://` path — most browsers block that download for security reasons when a page isn't served over `http://` or `https://`. The other five don't have this problem and will open fine either way.

To test everything, including the three that need a model download, serve this folder instead of opening the files directly:

```
cd path/to/this/folder
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser (not a `file://` link). Leave the Terminal window open while testing; closing it stops the server.

## Publishing to GitHub Pages

1. Create a new GitHub repository (or use an existing one set aside for this course).
2. Add every file in this folder to that repository, keeping them all at the same level (no subfolders).
3. In the repository's Settings → Pages, set the source to the main branch, root folder.
4. GitHub will publish the site at `https://[your-username].github.io/[repo-name]/`. `index.html` loads automatically at that address, no filename needed.
5. Update the `[ROOT]` placeholders in the flipbook (docx) with that address, and swap the flipbook's own hyperlinks or Heyzine hotspots to point at the individual activity pages.

Because every link in `index.html` and in the flipbook is a relative filename, nothing needs to change when moving from local testing to GitHub Pages, as long as all the files stay together in one folder (here, and one repository, there).

## AI disclosure

These activities and this README were curated by the author, developed with the assistance of Claude (Anthropic), Gemini, and NotebookLM, and reviewed before use.

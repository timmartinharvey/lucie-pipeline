# Lucie's Idea Pipeline

A small website for Lucie's content ideas. It's hosted free on GitHub Pages and keeps her choices (Shortlist, Planned, Filmed, Posted, Park) in this repo.

## Files

- `index.html`: the page.
- `ideas.json`: every idea with its full plan. The Monday run rewrites this file.
- `runs.json`: a summary of each Monday run.
- `statuses.json`: Lucie's choices, saved by the page. The Monday run reads this file but never edits it.
- `inbox.json`: ideas Lucie drops in at the bottom of the page. The Monday run marks each one as processed.
- `tools/build_data.py`: turns an export of the old pipeline database into `ideas.json` and `runs.json`.

## One-time setup (about 10 minutes)

1. On GitHub, create a new **public** repo called `lucie-pipeline` and upload everything in this folder.
2. In the repo, go to Settings > Pages. Set Source to "Deploy from a branch", choose `main` and `/ (root)`, then save. After a minute or two the site is live at `https://timmartinharvey.github.io/lucie-pipeline/`.
3. Make the save key: go to GitHub Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token.
   - Repository access: Only select repositories, then pick `lucie-pipeline`.
   - Permissions: Contents, Read and write. Leave everything else off.
   - Expiry: pick the longest you're happy with, and set a reminder to renew it.
4. Open the site on Lucie's phone, scroll to "Save key", paste the token and tap Save key. Do the same on any other device she uses. Add the page to her home screen with Share > Add to Home Screen.

## Things to know

- The repo is public, so anyone with the URL can read the ideas. Nothing in them names the older children or shows where she lives, but bear it in mind.
- The key only works on this one repo and only for its files. If a phone is lost, delete the token on GitHub and make a new one.
- Every tap creates a small commit (for example "Lucie: 2026-11-02-contact-nap-self-care to planned"), so the repo history is a full log of her choices.

# Working on the portfolio site (repo: portfolio)

This is T's public portfolio page. Its link is shared with recruiters, so it must never break.

## What it is

- One static page: `index.html`. No build step, no framework, no database.
- The same page also lives as T's Claude artifact "Tarakshya Mehrish"
  (https://claude.ai/artifact/XwqKeWzo2puRA7nMRr2vVp). Keep the two in sync: change one, change the other.
- Screenshots are inline images inside `index.html`. Fonts come from Google Fonts.
- No phone number on the page unless T explicitly asks for it.

## Release rule (set by the owner, T — not optional)

1. **Never commit or push directly to `main`.** `main` is what Vercel serves as the live site.
2. Every change goes on its own branch named `change/<short-description>`, pushed to GitHub.
3. Before handing over a preview, check the page at phone width (390 px) and wide (1366 px):
   nothing wider than the screen, every link works, back-to-top works.
4. Also force-push the branch to `review`, so T's fixed review link always shows the newest version.
   Give T a plain-English summary of what changed and what to look at.
5. **Stop and ask explicitly:** "Ready to make this live?" Only an explicit yes (e.g. "ship it") counts.
6. On approval: merge into `main`, push, confirm the production deployment is READY on the new commit.
   If `review` is behind `main`, force-push `main` to `review`.
7. If a live release breaks something, revert `main` first, then fix on a branch.

Explain things to T in plain language; T is a product person, not an engineer.

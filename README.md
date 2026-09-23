# Aptean Partner Hub — concept prototype

Static single-page prototype. No build step, no dependencies, no backend.

## Deploy to Vercel (CLI — fastest)

From inside this folder:

    npx vercel --prod

First run asks you to log in and confirm the project name. Accept the defaults;
it detects a static site automatically. You get a URL like
`aptean-partner-hub.vercel.app`.

To redeploy after any change, run the same command again.

## Deploy to Vercel (Git)

    git init && git add . && git commit -m "Partner Hub concept"
    gh repo create aptean-partner-hub --private --source=. --push

Then at vercel.com/new, import the repo. Framework preset: **Other**.
Build command: leave empty. Output directory: `.`

## Notes

- `vercel.json` sets `must-revalidate` so redeploys appear immediately rather
  than serving a cached copy.
- The page loads Inter from Google Fonts; everything else is inlined.
- Microphone dictation needs https, which Vercel gives you — it does not work
  from a local file.

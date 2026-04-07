# Portfolio Dashboard with Netlify Proxy

## Why this package
GitHub Pages/static-only hosting hit browser CORS errors. This version keeps the frontend static, but moves the EODHD calls into a Netlify Function.

## Files
- `index.html` — static frontend
- `netlify/functions/quotes.js` — serverless proxy endpoint
- `netlify.toml` — tells Netlify where the functions folder is

## Deploy to Netlify
1. Create a new GitHub repository.
2. Upload all files from this ZIP, keeping the folder structure exactly as-is.
3. Log in to Netlify.
4. Choose **Add new site** → **Import an existing project**.
5. Connect GitHub and select your repository.
6. Netlify should detect `netlify.toml` automatically.
7. Deploy the site.

## Use
- Open the deployed Netlify URL.
- Paste your EODHD API key into the page.
- Add holdings and click Refresh quotes.

## Notes
- TASE prices are divided by 100 for calculations.
- USD/ILS is fetched automatically via `USDILS.FOREX`.
- Browser CORS is avoided because the browser calls your Netlify function instead of EODHD directly.

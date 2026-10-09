# Outlet performance dashboard

Weekly sales vs target for Tampines, Jurong and Orchard, read from the Supabase table `outlet_weekly`. If Supabase can't be reached, it shows the built-in sample data instead; the subtitle says which source is in use.

## Run locally

```bash
npm install
cp .env.example .env
npm run dev
```

## Deploy to Vercel

1. Import this repository in Vercel. It detects Vite automatically (build command `npm run build`, output folder `dist`).
2. Under Settings > Environment Variables, add `VITE_SUPABASE_URL` and `VITE_SUPABASE_PUBLISHABLE_KEY` with the values from `.env.example`.
3. Deploy. If the variables were added after the first deploy, redeploy so the build picks them up.

## Where things are

- `src/data.js`: `loadData()`, the only place data is fetched.
- `src/main.js`: KPIs, filter, bars and the "Needs attention" list.
- `src/style.css`: styles.

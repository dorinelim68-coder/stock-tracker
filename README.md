# Outlet performance dashboard

Single-page dashboard (`index.html`) showing sales vs target per outlet-week.
Static site: no build step. Data and sign-in come from Supabase.

## Deploy on Vercel
1. Import this repo in Vercel (New Project).
2. Framework Preset: **Other**. Leave Build Command and Output Directory empty, Root Directory `./`.
3. Deploy.

## Supabase
- Project URL and publishable key are set at the top of the script in `index.html` (`SUPABASE_URL`, `SUPABASE_KEY`). The publishable key is designed to be public; access is enforced by Row Level Security.
- Tables: `public.outlet_weeks`, `public.profiles` (plus Supabase `auth.users`).
- Users sign in with a username, which maps to `<username>@outlets.local`.
- In Supabase, Authentication > URL Configuration, add your Vercel URL as the Site URL.
- Change the default passwords before real use.

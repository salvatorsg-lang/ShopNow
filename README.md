# J's Garage Sale — site files

Simple one-page garage sale site. All 8 active Carousell items, with the
DDPAI Z60 in full detail. Built 2026-11-10. Zero cost to run: Vercel free
tier + Google Search Console free.

## Files

- `index.html` — the page: index of all 8 items, DDPAI in full detail,
  title, meta description, Open Graph tags, ItemList + Product
  structured data for Google
- `styles.css` — styling, mobile-first
- `ddpai-box-front.jpg`, `ddpai-box-back.jpg`, `ddpai-cameras.jpg` —
  the 3 real DDPAI photos (kept at the root, next to index.html —
  that is how they are uploaded in the repo, so index.html points
  at them directly, no `images/` folder)
- `ddpai-z60-ad-21s.mp4` — the 21-second DDPAI video, also at the root
- `sitemap.xml` — update the `<loc>` URL after deploying, then submit it
  in Search Console
- `robots.txt` — allows all search engines

## Items on the page

1. DDPAI Z60 4K 3-Channel Dashcam Set — S$338 (full detail + photos + video)
2. Pioneer Car Audio Bundle, TS-G1620F-2 + TS-WX700DA subwoofer — S$338
3. iDrive i11 Dash Cam (Front + Rear) Full Set — S$88
4. Wireless CarPlay & Android Auto Adapter — S$68
5. Phottix Nuada P LED Light Panel, Full Set — S$55
6. AVANSTAR AS250 LED Headlight H11/6000K — S$50
7. Fisher Price Walker — S$20
8. Magnetic Mobile Phone Holder — S$18

Total if everything sells: S$975. Items 2–8 link to the Carousell
profile (https://www.carousell.sg/u/clickgift/) for photos and details —
send their photos to add them to the page itself.

## Upload to Vercel (free, no cost)

Option A — GitHub (recommended, auto-deploys on every change):
1. Create a new GitHub repo, e.g. `garage-sale`, and upload these files
   (same web upload as the portfolio site: unzip first, upload the files).
2. Go to vercel.com, sign up free, Add New Project, Import the repo.
3. Vercel gives a free address like `garage-sale.vercel.app`. Done.

Option B — drag and drop:
1. Go to vercel.com, sign up free, Add New Project.
2. Drag the unzipped folder onto the deploy area. Same free address.

## After deploying — Google, zero cost

1. Replace `https://example.com/` in `sitemap.xml` with the real site
   address (and update the address in this README). Also add a
   `<link rel="canonical">` in `index.html` with the real address.
2. In Google Search Console, add the new site as a URL-prefix property
   and verify with the HTML file method (same as the portfolio site —
   DNS verification does not work for hosted subdomains you don't own).
   Upload the verification file to the repo and wait for the deploy,
   then press VERIFY.
3. In Search Console, submit the sitemap and request indexing for the
   homepage. Indexing takes days, not minutes — check back in Search
   Console under Pages and Performance to see what Google found.

## Adding items or photos

Copy a `<section class="item-mini">` block in `index.html` for a new
item, and add a matching line in the index list at the top and a
matching Product block in the structured data. Put its photos in the
repo root next to index.html (flat layout) and reference them by
file name, like the DDPAI ones.

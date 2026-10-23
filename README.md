# Octoberside

Saturday, Oct 24 · 12 stops from Hopkins to Nordeast Minneapolis.

Open `index.html` for the interactive map. Hover or tap a pin for arrival time, hours, notes and a link to the bar's Google Maps page.

## Publish with GitHub Pages
1. Push this folder to a repo.
2. Go to Settings → Pages, set the source to the `main` branch, root folder, and save.
3. The site is live at `https://<your-username>.github.io/<repo-name>/`.

## Add photos to a bar's tab
Upload pictures into the `images/` folder named after the bar's id, numbered 1 to 4:

    images/nyes-1.jpg   images/nyes-2.jpg   ...

Bar ids: mainstreet, cuzzys, nyes, moose, yacht, 1029, dustys, knightcap, shaws, jimmys, palace, grumpys.
They show up on that bar's tab automatically.

## Put it on your home screen
Open the GitHub Pages link on your phone (not the downloaded file).
- iPhone (Safari): tap Share, then Add to Home Screen.
- Android (Chrome): tap the ⋮ menu, then Add to Home screen or Install app.
It opens full screen with its own icon, and the stop list still loads if bar signal drops.

## Live scoring (scorekeeper only)
Everything is stored in `counts.json`, and crawl photos go in `images/crawl/`. Everyone can see them; only the phone holding your GitHub key can change them.

Make the key:
1. On GitHub: your profile picture → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token.
2. Name it `octoberside`, expiration 7 days, Repository access "Only select repositories" → `octoberside`.
3. Repository permissions → Contents → "Read and write". Generate and copy it.
4. In the Octoberside home-screen app, tap the Octoberside title 5 times, paste the key, tap Sign in.

What you get once signed in:
- On each bar's tab: "We're here" and "We're leaving" buttons (records the time), +1 / −1 beer buttons for each guy at that bar, and tap a guy's face or name to take his photo.
- On the Route tab: +1 / −1 buttons that add to whichever bar you're at.
- "+ Add a stop that's not on the plan" on the Route tab: type the bar name and it becomes a new tab after the bar you're at. Off-plan stops have a "Remove this stop" button.
- Tapping "We're here" at a bar automatically marks the previous bar as left.

Planned bars you never arrive at show as skipped once you've moved past them. Running totals follow the order you actually visit, and milestones trigger when each guy hits the beer count, wherever you are.

## Heads
Upload one photo per guy to `images/heads/`, named `bret.png`, `travis.png`, `greg.png`. After someone's first crawl photo, the newest crawl photo is used instead.

## Bets (Google Form)
Bets come from a Google Form so anyone can bet without a GitHub account. The Bets tab reads the results and does the math. Betting closes at 2:00 PM Saturday; bets stamped later are ignored.

1. Go to forms.google.com → Blank form. Title it "Octoberside bets".
2. Add these questions, all Short answer, none required, titled exactly:
   Your name · Bret · Travis · Greg · Heckle who · At beer # · Comment
3. Settings → Responses: make sure sign-in is NOT required.
4. Responses tab → Link to Sheets → create a new sheet.
5. In the sheet: Share → General access → "Anyone with the link" → Viewer. Then File → Settings → Time zone → (GMT-05:00) Central Time - Chicago.
6. Back in the form: ⋮ menu → Get pre-filled link → type 1 in every box → Get link → Copy link.
7. Send Claude (or paste into the BETS block in index.html): the pre-filled link and the sheet's link.

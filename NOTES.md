Phase 1 one-pager (final)

Problem: Mid-handicap golfers don't know their real numbers (carry, miss pattern) or where they lose shots, so they play and practice on guesswork.

User: A regular mid-handicapper who pays for one launch monitor session to understand their game.

Core idea: Turn one TrackMan session plus simple round logging into a personal profile that powers caddy-style advice and a practice plan.

MVP features (web, proof of concept):

Import TrackMan CSV into a bag profile: carry, left/right miss and spread per club, with 3/4 shots separate.
Gapping view that flags overlapping clubs (like your 3 iron, 4 iron and 4 hybrid).
Shot advisor: enter yardage, wind and hazards, and get a club, an aim point and a short reason.
Round logger: per hole fairway, green in regulation, putts and penalties.
Where am I losing shots?: a simple analysis from the round logs and a few practice priorities.

Out of scope for now: live launch monitor links, accounts and payments, mobile app, true strokes gained. I also parked GPS and course maps for v2, since I saw your project is about a GPS app. Tell me if you'd rather that be in v1.

Success test: You use it yourself for a few rounds and the advice feels more right than your gut.

Phase 2: tools and tech stack

Suggested setup, all free:

Web app only, no backend. Data stays in the browser, so there are no servers, logins or hosting bills.
Stack: plain HTML, CSS and JavaScript to start, which is easiest to learn and debug. A CSV library like Papa Parse can handle your semicolon and comma-decimal file.
The "AI" part: the club math (carry, wind adjustments, miss pattern) is plain code, which is faster, free and predictable. Claude can later write the explanations and practice plans, but that needs a small backend to protect the API key, so we add it after the core works.
Hosting: Vercel, Netlify or GitHub Pages, all free.
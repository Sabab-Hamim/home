========================================================
  SABAB HAMIM — LINK PROFILE  |  Customisation Guide
========================================================

FOLDER STRUCTURE
----------------
  index.html          ← Main page (edit content here)
  style.css           ← All styles (edit colours/fonts here)
  images/
    profile/          ← Put your profile photo here
    games/            ← Put game cover icons here
  README.txt          ← This file


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. PROFILE PHOTO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Place your photo at:
  images/profile/photo.jpg

Supported formats: .jpg  .jpeg  .png  .webp
Recommended size:  400×400 px or larger (square crop)

If the file is missing, your initials ("SH") are shown
as a fallback automatically — no code change needed.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
2. NAME, HANDLE & BIO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Open index.html and find:

  <h1 class="name">Sabab Hamim</h1>
  <p class="handle">@sabab.exe</p>
  <p class="bio">Tech Enthusiast · Developer · Gamer<br>
                 Crafting experiences that feel alive.</p>

Replace the text between the tags with your own.
Use <br> for a line break inside the bio.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
3. TAGS (the small pills under your bio)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Find the <div class="tags"> block:

  <div class="tags">
    <span class="tag">UI/UX</span>
    <span class="tag">Full-Stack</span>
    ...
  </div>

Add, remove or rename <span class="tag">...</span> items.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
4. NOW PLAYING (music widget)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Find:

  <div class="music-title">Blinding Lights</div>
  <div class="music-artist">The Weeknd · listening now</div>

Change the song title and artist to whatever you like.
To hide this widget entirely, delete the whole
<div class="now-playing">...</div> block.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
5. SOCIAL LINKS  ("Find me on")
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Each link looks like this:

  <a class="link-btn" href="https://facebook.com/yourhandle"
     target="_blank" rel="noopener">
    ...
    <span class="link-label">Facebook
      <span class="link-sub">Profile & updates</span>
    </span>
    ...
  </a>

  ▸ Change the href="..." URL to your real profile link.
  ▸ Change the label text if you want.
  ▸ To remove a platform, delete the whole <a ...></a> block.
  ▸ To add a platform, copy an existing block and replace
    the href, label, sub-label, and SVG icon path.

Current order: Facebook → Instagram → Twitter/X →
               LinkedIn → Anonymous Ask (NGL)

For Anonymous Ask, replace the NGL link with your
own NGL / Retrospring / CuriousCat URL:
  href="https://ngl.link/yourhandle"


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
6. CURRENTLY PLAYING GAMES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Game icons are 54×54 px rounded squares.

Step 1 — add your icon image:
  Place it in  images/games/
  Example:  images/games/valorant.jpg

Step 2 — add a block in index.html inside
  <div class="games-grid">:

  <div class="game-icon-wrap" title="Game Name">
    <img src="images/games/yourfile.jpg" alt="Game Name"
         onerror="this.style.display='none';
                  this.parentElement.innerHTML=
                  '<div class=\'game-icon-placeholder\'>🎮</div>'"/>
  </div>

  ▸ Change title="..." to the game name (shown on hover).
  ▸ Change src="..." to the path of your icon.
  ▸ Change the emoji in the onerror fallback if you like.

To remove a game, delete its <div class="game-icon-wrap">
...  </div> block.

Recommended image size: 128×128 px minimum, square.
Supported formats: .jpg  .png  .webp


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
7. CONTACT INFO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Find the two contact cards.

For email — update both the onclick value and the
displayed text:

  <div class="contact-card"
       onclick="copyText('your@email.com','email-chip')">
    ...
    <div class="contact-value">your@email.com</div>
    ...
    <button ... onclick="...copyText('your@email.com',...)">

For phone — same pattern:

  onclick="copyText('+880 XXXX XXXXXX','phone-chip')"
  <div class="contact-value">+880 XXXX XXXXXX</div>


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
8. FOOTER TEXT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Find near the bottom of index.html:

  <p class="footer" ...>© 2026 · Sabab Hamim · Made with ♥</p>

Change the year and name as needed.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
9. COLOURS & THEME  (style.css)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
All colours are CSS variables at the top of style.css.

Dark theme block:   [data-theme="dark"]  { ... }
Light theme block:  [data-theme="light"] { ... }

Key variables:
  --bg          Page background
  --text        Main text colour
  --p1          Primary accent (purple tones)
  --p2          Secondary accent
  --p3          Tertiary accent
  --surface     Card / button background
  --border      Border colour
  --muted       Subdued text

Change any hex value to customise the palette.
The site automatically uses the right variable
for each theme.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
10. DEFAULT THEME  (dark or light on first load)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
In index.html, first line of <html>:

  <html lang="en" data-theme="dark">

Change "dark" to "light" to default to light mode.
After the user toggles, their choice is saved in
localStorage and respected on future visits.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
11. PAGE TITLE & TAB NAME
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
In index.html inside <head>:

  <title>Sabab Hamim</title>

Change to your name or preferred title.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
QUICK CHECKLIST BEFORE GOING LIVE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  [ ] Profile photo added to  images/profile/photo.jpg
  [ ] All social links updated with real URLs
  [ ] Anonymous Ask link updated
  [ ] Game icons added to  images/games/
  [ ] Email and phone updated in both onclick and display
  [ ] Footer year and name updated
  [ ] Page <title> updated

========================================================

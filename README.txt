BhojanGo — Complete Source Package
===================================

WHAT'S INSIDE
-------------
index.html        The complete website (HTML + CSS + JavaScript in one file)
images/           All 124 images used by the site, in PNG format
README.txt        This file

IMAGES FOLDER (124 PNG files)
------------------------------
- 122 dish photos, one per menu item, named after the dish ID
  (e.g. biryani.png, butter-chicken.png, baklava.png, etc.)
- bhojango-logo.png   — the BhojanGo logo shown in the header and footer
- payment-qr.png      — the QR code shown on the "Scan & Pay" checkout screen

HOW TO USE
----------
1. Keep index.html and the images/ folder together in the same directory —
   the page loads photos using relative paths like "images/biryani.png",
   so if the images folder is moved or renamed, the photos won't show.
2. Double-click index.html to open the site in any browser. No server,
   build step, or internet connection is required for the core site to
   work (though a few features listed below do need internet access).
3. To host it online, upload both index.html and the images/ folder to
   your web host, keeping the same relative structure.

FEATURES THAT NEED INTERNET ACCESS
-----------------------------------
Most of the site works fully offline, but these specific features call
external services and will only work when the device has an internet
connection:
- Google Fonts (Anton, Space Mono, Inter) — falls back to system fonts
  if unavailable
- Leaflet map tiles (OpenStreetMap) — used for the address picker under
  Sign In → delivery address, and the restaurant partner signup map
- Nominatim address search/autocomplete — powers the address search box
  and "use my current location" reverse-geocoding

CURRENT SITE FEATURES
----------------------
- Full menu across 9 stalls, 122 dishes, all with real photos
- Veg / Non-Veg filter with the standard green/red indicator on each dish
- Cart, checkout, and live order tracking with a kitchen-ticket UI
- Pay Online (QR code) or Cash on Delivery
- Delivery rider assignment with name, phone (call/message links), and ETA
- Customer sign-in (name + phone + OTP) with an interactive map-based
  address picker (search-as-you-type + draggable pin + use-my-location)
- Restaurant Partner sign up / log in, with the same map address picker
- Animated hero banner with a live scrolling menu ticker

EDITING THE SITE
----------------
- Menu items, prices, and stall info live in the STALLS array near the
  top of the <script> section in index.html.
- Dish photos are referenced by ID in the REAL_PHOTOS object — matching
  filenames in the images/ folder.
- All styling is in the <style> block at the top of index.html.

This is a front-end demo/prototype: order flow, payments, OTP login, and
delivery tracking are all simulated in the browser with no real backend,
database, or payment processor behind them.

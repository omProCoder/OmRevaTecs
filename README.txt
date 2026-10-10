RAJLAXMI REVATECs WEB APP
Open index.html in a browser. It is responsive for desktop and mobile.

WHAT'S IN THIS VERSION
- Real contact details are filled in: phone/WhatsApp +91 94237 17855, email rajlaxmi.omrevatecs@gmail.com
- Mobile hamburger menu: nav links now collapse into a ☰ button under 800px width instead of disappearing
- Enquiry form is wired: on submit it opens WhatsApp (wa.me) with the visitor's name, phone,
  service and requirement pre-filled as a message, so enquiries land directly in your WhatsApp.
  A "write to us instead" email link is offered as a fallback next to the button.
- Form fields now have proper name/type/autocomplete attributes and labels linked to inputs
  (better accessibility and mobile keyboard behaviour, e.g. numeric keypad for phone).
- Added meta description, Open Graph tags and a favicon for better link previews and SEO.
- Wrapped page content in a <main> landmark for accessibility.

THIS IS NOW AN INSTALLABLE APP (PWA)
Files added: manifest.json, sw.js (service worker), icon-192.png, icon-512.png, icon-512-maskable.png.
Upload ALL these files together, in the same folder, to your web hosting (same folder as index.html).
Once it's live on https://yourdomain.com:
- On Android Chrome, visitors get an "Install app" / "Add to Home Screen" prompt automatically.
- On iPhone Safari, visitors tap Share -> "Add to Home Screen".
Either way it opens full-screen with your icon, no browser bar, and works offline after the first visit.
This does NOT require the Play Store and needs no approval process.

WANT AN ACTUAL .APK / PLAY STORE LISTING?
Once the site above is live at a real URL, go to https://www.pwabuilder.com, paste your URL,
and it will package this PWA into a signed Android APK/AAB you can install directly or submit
to the Play Store. It's free and takes a few minutes. (It needs your site to be actually hosted
online first — it can't package files sitting on your computer.)

IF YOU WANT A REAL BACKEND LATER
The WhatsApp handoff works with no server at all, so this is deploy-ready as-is.
If you later want enquiries to also save to a database or send an auto-email, that submit
handler in the <script> at the bottom of index.html is the place to add a fetch() call to
your backend or a form service (e.g. Formspree, Google Sheets via Apps Script, etc).

RENDER DEPLOYMENT
-----------------
This package includes package.json and server.js so it can be deployed directly as a Render Web Service.
Build command: npm install
Start command: npm start
The server listens on Render's PORT environment variable.

Alternatively, use render.yaml for the included deployment configuration.

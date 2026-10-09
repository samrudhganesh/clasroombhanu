# Classroom – classroom management platform

Zero-build static app. Open `index.html` (or `npx serve .`). Data persists in browser localStorage.

Demo logins: instructor@demo.edu / Teach123!  ·  ananya@demo.edu / Learn123!
Add a student as instructor to get a temp password; sign in with it on the Student tab to see the forced password change.

## Font
Google Sans Product is proprietary and not on Google Fonts. Put licensed files in `fonts/` as
`GoogleSansProduct-{Regular,Medium,Bold}.woff2`. Until then the app falls back to Google Sans (Google Fonts).

## Going to production
This is a client-side build: passwords are SHA-256 hashed and sessions live in the browser, which is NOT secure
against a real attacker. Replace the `DB`/`save()` layer with a backend (salted bcrypt/argon2, server sessions,
signed-URL file storage with virus scanning, email delivery, Google OAuth, websockets). UI and flows carry over.
File attachments record only the filename here.

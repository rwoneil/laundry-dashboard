# Laundry Dashboard — configured for Firebase

This version includes your Firebase Realtime Database URL and web app configuration.

## Before deploying

In Firebase Console > Realtime Database > Rules, publish the contents of `database.rules.json`. These permissive rules are for a low-stakes household prototype only: anyone with the database URL can modify or delete all machine and history data. Do not store personal information.

## Deploy with Firebase Hosting

1. Install Node.js if needed.
2. In Terminal: `npm install -g firebase-tools` then `firebase login`.
3. Unzip this archive, open Terminal in the extracted folder (the folder containing `index.html` and `firebase.json`).
4. Run `firebase deploy --only hosting --project laundry-dashboard-19fd5`.
5. Open the Hosting URL printed by Firebase. Test from two phones.

If Firebase reports permission errors, check the Realtime Database Rules tab. This is not a secure deployment: no user authentication is implemented.

The dashboard logs historical events but does not yet chart popular times. Timers are estimates, not connected to appliances.

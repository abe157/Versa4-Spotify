# Spotify Fitbit App for Versa 4

This is source code for the Spotify HR on the Fitbit Versa 4.

🚧 All content within this repository is provided for educational purposes only. Use at your own risk. 🚧

![Demo](./screenshots/app.png)

## Features

The app is a remote controller for your Spotify account.

- Remote control music playback
- Change playlist
- Volume control

## Why *HR*?

HR stands for Heart-Rate. Spotify HR implements a unique Heart-Rate based shuffle feature.
When enabled the songs in your current playlist will be shuffled to match your current heart rate during playback.
With faster and higher tempo songs being played as your heart rate increases.
A nice addition to enjoy matching music to any varied workout.

![HR Shuffle](./screenshots/hr.png)

## Common Issues

### No active device found

Please ensure that:

- Your Fitbit device is connected to your phone via Bluetooth and Fitbit app is running in the background.
- That Spotify is running and open on your device.
- That you’ve logged into the same Spotify account on Fitbit and on the Spotify app.

### Playback controls are not working

Unfortunately controlling playback requires a Premium Spotify account. This is restriction imposed by the Spotify Web API.

### Lost connection to Fitbit app

This usually happens when the Spotify app cannot communicate with the Fitbit app on your iOS/Android device.

Please ensure that:

- Bluetooth is enabled on your phone and the watch is connected via Bluetooth
- The Fitbit app is running and has permission to run in the background

If it's still not working, please open the Fitbit app on your phone and sync your Fitbit by dragging down on the main screen.

### Logged in to wrong account

1. [Visit Spotify in your browser](https://www.spotify.com/)
2. Click “Log Out” from the menu
3. Open the Fitbit app, go to Spotify HR settings and log in again.


## Getting Started

1. Create a spotify [developer](https://developer.spotify.com/dashboard/a) account and create an app.
    1. note the clientID and client secret to put into the `common/spotify.secret.js`.
    1. Include the redirect URL (https://app-settings.fitbitdevelopercontent.com/simple-redirect.html) in the spotify developer app after creating one.

1. Side-load the app.
```bash
$ npx fitbit
fitbit$ build-and-install
```

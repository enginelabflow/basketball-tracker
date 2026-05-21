# Basketball Game Metrics Tracker

A lightweight, single-file HTML web app for tracking basketball game development metrics during or after a game.

The tracker focuses on whether the game created useful development reps: usable touches, safe passing windows, trust points, quick decisions, and related review markers.

## Features

- Track game name and date
- Increment or decrement each metric with large tap-friendly controls
- See a fixed bottom tally of the key counts
- Copy a formatted game summary for notes or review
- Clear all metrics for a new game
- Automatically saves progress in the browser with `localStorage`
- Runs entirely from one HTML file with no build step or dependencies

## Metrics

The app currently tracks:

- Minutes Played
- Usable Touches
- Safe Passing Windows
- Open But Not Passed
- Trust Points
- Shot Attempts
- Quick Decisions
- Clips Captured

## How To Use

Open `basketball-tracker.html` in a browser.

You can double-click the file, or open it from a terminal:

```powershell
start .\basketball-tracker.html
```

Enter the game name and date, then use the plus and minus buttons to update each metric. Use **Copy** to copy a review summary, or **Clear** to reset the tracker for the next game.

## Data Storage

Data is saved locally in the browser under the `basketball-game-metrics-v1` storage key. It stays on the device and browser where the app is used.

Clearing browser site data or using a different browser/device will remove or hide the saved tracker state.

## Customizing Metrics

To change the tracked metrics, edit the `metrics` array inside `basketball-tracker.html`.

Each metric has:

- `id`: internal storage key
- `name`: label shown in the app
- `help`: short description shown below the label


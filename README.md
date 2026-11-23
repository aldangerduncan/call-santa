# Call Santa

A single page web app that puts a child through to Santa Claus on a voice call,
built on an ElevenLabs conversational agent. Designed to be added to an iPhone
home screen so it looks and behaves like a standalone app.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app. Night sky, snow, and the embedded ElevenLabs widget. |
| `manifest.json` | Web app manifest, for Android and for standalone display. |
| `apple-touch-icon.png` | 180px home screen icon for iOS. |
| `icon-192.png`, `icon-512.png` | Manifest icons, also used as the artwork on the page. |
| `.nojekyll` | Stops GitHub Pages running the files through Jekyll. |

## Turning on GitHub Pages

1. Go to Settings, then Pages.
2. Under Source choose "Deploy from a branch".
3. Pick branch `main` and folder `/ (root)`, then Save.
4. Wait about a minute. The URL appears at the top of that same page.

Pages requires a public repository on a free GitHub plan.

## Adding it to the home screen on iOS

1. Open the Pages URL in Safari. It must be Safari, not Chrome.
2. Tap Share, then "Add to Home Screen".
3. Open it from the new icon, not from Safari, and allow the microphone when asked.

Standalone mode asks for microphone permission separately from Safari, so grant
it the first time you open it from the icon.

## Changing what Santa says

Everything about Santa lives in the ElevenLabs agent, not in this repo. Edit the
agent's system prompt, voice or guardrails in the ElevenLabs dashboard. The only
thing this page holds is the agent ID in `index.html`.

## Locking it down

The agent accepts calls from anyone holding its ID, and that ID is visible in the
page source. Once the Pages URL exists, add that hostname to the agent's allowlist
in ElevenLabs so no other site can embed it.

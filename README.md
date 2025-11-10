# Chat App

A simple web chat application (front-end + Node server). This repository contains a small chat front-end in `public/` and a Node-based server in `src/` with utility helpers in `utils/`.

## Quick overview

- Frontend: `public/` — HTML, CSS, and client-side JavaScript (`public/js/chat.js`).
- Server: `src/index.js` — Node server entry point (may use Express / socket library depending on implementation).
- Utilities: `utils/messages.js` — message helper(s).
- Other: `package.json` — project metadata and npm scripts.

## Contract (what this repo provides)

- Inputs: HTTP/WebSocket connections from browser clients.
- Outputs: Real-time chat messages broadcast to connected clients and simple message persistence/formatting via utilities.
- Success criteria: App runs locally, clients can connect and exchange messages.
- Error modes: Server not started, port in use, missing dependencies.

## Prerequisites

- Node.js (v14+ recommended)
- npm (comes with Node)
- A modern web browser

## Install

Open a PowerShell window in the project root (`c:\Users\ROK TECH\Desktop\Chat App`) and run:

```powershell
npm install
```

This installs dependencies listed in `package.json`.

## Run (common options)

If a start script exists in `package.json` (common):

```powershell
npm start
```

If there is no `start` script, run the server directly (assumes server entry is `src/index.js`):

```powershell
node src/index.js
```

Once the server is running, open the browser and navigate to the server URL (commonly `http://localhost:3000` or the port printed by the server). If this project is a purely static front-end, open `public/index.html` in the browser.

Note: Check `src/index.js` for the configured port and any additional startup instructions.

## Development notes / Files of interest

- `public/index.html` — main HTML file for the client.
- `public/css/styles.css` — styling.
- `public/js/chat.js` — client-side chat logic and UI handling.
- `src/index.js` — server entrypoint (HTTP server and real-time message handling).
- `utils/messages.js` — message formatting and helper functions.
- `package.json` — scripts and dependencies.

## How to test locally

- Install dependencies
- Start the server (`npm start` or `node src/index.js`)
- Open two browser windows/tabs and connect to the app URL to verify messages are delivered between clients.

## Edge cases & tips

- Empty messages: The client should prevent sending blank messages — see `public/js/chat.js`.
- Large message volumes: This sample app is not optimized for heavy traffic or persistence; consider adding database storage for production.
- Port conflicts: If the chosen port is in use, edit `src/index.js` or set an environment variable (check file) to choose a different port.

## Next steps / suggestions

- Add tests (unit tests for `utils/messages.js`, and simple integration tests for server endpoints).
- Add a `start` script to `package.json` if missing.
- Add a CONTRIBUTING guide and screenshots in `docs/`.
- Add a license file (e.g., `LICENSE`) if you plan to publish.

## Contributing

Contributions welcome. Open an issue or submit a pull request describing the change.

## License

This project does not include a license file. Add a `LICENSE` to make the terms explicit.

---

If you'd like, I can also:

- insert a `start` script into `package.json` (I can check it first),
- add a sample `LICENSE` (MIT) and a small test for `utils/messages.js`,
- or include screenshots and small usage GIFs in `public/assets/`.

Tell me which follow-up you'd like and I'll continue.

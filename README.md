# Drelvix

**A fast, private API client for developers.** Build, send, inspect, save and test API requests in one place, on desktop, web, tablet and phone.

Drelvix works fully offline with no account. Sign in only if you want your collections synced across devices or shared with teammates.

[//]: # (<!-- Add a hero screenshot: ![Drelvix workspace]&#40;docs/screenshots/workspace.png&#41; -->)

---

## Why Drelvix

- **Local-first.** Everything is stored on your device. No sign-up, no server needed to send a request.
- **Private by design.** No ads, no analytics, no telemetry. Secrets stay in your operating system's secure storage.
- **Familiar workflow.** Collections, environments, variables and tabs, laid out the way you expect from a modern API client.
- **Runs everywhere.** Windows, macOS, Linux, web, tablet or even android.
- **Dark theme, done properly.** One carefully tuned dark look, easy on the eyes during long sessions.

---

## Features

### Build and send requests
- All standard methods: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `HEAD`, `OPTIONS`
- Query parameters, headers and form fields with a toggle on every row
- Request bodies: **JSON**, raw text, `x-www-form-urlencoded`, `multipart/form-data` (text fields) and **GraphQL** (query plus variables)
- Send and cancel, with protection against accidental double submits
- Per-request timeout and redirect control, plus an app-wide default timeout
- Plain-language errors for DNS failures, TLS problems, timeouts, refused connections and malformed responses

### Authentication
- No auth, Bearer token, Basic auth and API key (header or query parameter)
- Set auth once on a collection and let requests inherit it
- Warning when an API key would travel in the URL

### Inspect responses
- Status, time and size at a glance
- **Pretty, colorized JSON** with a raw view
- Search inside the body with highlighting
- Searchable headers, a parsed cookies view and response metadata
- Copy the body or the full details in one click
- Save any response as an example attached to the request

### Collections and organization
- Collections with nested folders
- Rename, duplicate, move and reorder
- Favorites, tags and search by name, URL or tag
- Collection defaults: description, auth, headers and variables
- Request descriptions and saved response examples

### Environments and variables
- Environment profiles such as Local, Dev, Staging and Prod, with a quick switcher in the toolbar
- Use `{{variable}}` in URLs, headers, parameters, auth and bodies
- Clear precedence: **session → collection → environment → global**
- **Secret variables** that are masked and never written to the database, exports or cloud sync
- Dynamic variables: `{{$timestamp}}`, `{{$isoTimestamp}}`, `{{$randomUUID}}`, `{{$randomInt}}`
- Variables are highlighted as you type; hover one to see its value and where it comes from
- Preview of the fully resolved request before you send it

### Tests and chaining
- Assertions on status code, response time, headers and JSON values
- Pass/fail results with a clear explanation of every failure
- Request chaining: pull a value out of one response and use it in the next request

### History
- Every request you send is recorded with method, URL, status and duration
- Replay with one click
- Filter by URL, method, status class and date
- Privacy controls: mask sensitive headers, skip storing bodies, and limit how many entries are kept

### Import, export and code snippets
- **Postman** collection import (v2.x), from a file or pasted JSON, with a report of anything that could not be imported
- **cURL** import and export
- **Drelvix backup** export and import, validated and versioned
- Generate code snippets for cURL, JavaScript (`fetch`) and Python (`requests`)

### Optional cloud sync and sharing
- Sign in with an emailed link or code, or with GitHub
- Syncs structured data only: collections, folders, requests, environments and non-secret variables
- Never syncs secrets, media, files or exports
- Works offline and syncs in the background when you are connected
- Conflicts are flagged and you choose which version to keep
- Invite people to a single collection by email with **owner**, **editor** or **viewer** access

### Workspace and ergonomics
- Resizable panes; collapse the sidebar or the response panel to focus
- Stacked or side-by-side request and response layout
- Responsive on every screen size, from a phone to a wide desktop monitor
- Your in-progress request survives an app restart
- Keyboard shortcuts: `Ctrl/Cmd + Enter` to send, `Ctrl/Cmd + S` to save, `Ctrl/Cmd + N` for a new request

---

## Security and privacy

| | |
|---|---|
| **Certificates** | TLS is always validated. Drelvix never silently disables certificate checks, and ignores `--insecure` on cURL import. |
| **Secrets** | Tokens, passwords, API keys and secret variables are stored in your OS keychain or secure store, not in the database. |
| **Exports and sync** | Secrets are never included in backups or cloud sync. Exports show a warning, since URLs, headers and bodies are included as written. |
| **History** | Authorization, Cookie and API-key headers can be masked, and request bodies can be left out. |
| **Tracking** | None. No analytics, ads or third-party SDKs. |
| **Your data** | Clear all local data, and delete your cloud data, from Settings at any time. |

---

## Platforms

| Platform | Status |
|---|---|
| Windows, macOS, Linux | Supported |
| Web | Supported |
| Tablet | Supported |
| Phone (Android, iOS) | Supported |

Desktop and web are the primary experience; tablet and phone use the same app adapted to smaller screens.

---

## Screenshots

<!--
![Workspace](docs/screenshots/workspace.png)
![Environments](docs/screenshots/environments.png)
![History](docs/screenshots/history.png)
![Mobile](docs/screenshots/mobile.png)
-->

---

## Roadmap

Not available yet, and planned for later releases:

- OAuth 2.0
- File and binary request bodies
- Persistent cookie jar
- Folder-level authentication
- Response comparison and table view
- Collection runner and data-driven runs
- OpenAPI import
- App lock with biometrics or PIN
- WebSocket, Server-Sent Events and gRPC

---

## FAQ

**Do I need an account?**
No. Everything works offline without signing in. An account is only for sync and sharing.

**Where is my data stored?**
On your device. If you turn on sync, structured data (collections, requests, environments) is also stored in your own cloud project.

**Are my API keys and tokens synced?**
No. Secrets stay on the device that entered them.

**Can I move from Postman?**
Yes. Import a Postman v2.x collection from a file. Scripts and some auth types are not imported, and the import report tells you exactly what was skipped.

**Does Drelvix collect usage data?**
No.

---

## Contributing and feedback

Found a bug or have an idea? Please open an issue on the repository's **Issues** tab and include your platform and what you expected to happen.

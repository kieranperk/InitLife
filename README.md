<div align="center">

```
██╗███╗   ██╗██╗████████╗██╗     ██╗███████╗███████╗
██║████╗  ██║██║╚══██╔══╝██║     ██║██╔════╝██╔════╝
██║██╔██╗ ██║██║   ██║   ██║     ██║█████╗  █████╗  
██║██║╚██╗██║██║   ██║   ██║     ██║██╔══╝  ██╔══╝  
██║██║ ╚████║██║   ██║   ███████╗██║██║     ███████╗
╚═╝╚═╝  ╚═══╝╚═╝   ╚═╝   ╚══════╝╚═╝╚═╝     ╚══════╝
```

**your life. one terminal.**

[![Live](https://img.shields.io/badge/live-initlife.app-white?style=flat-square&labelColor=black)](https://initlife.app)
[![License](https://img.shields.io/badge/license-MIT--Commons_Clause-white?style=flat-square&labelColor=black)](#license)
[![Version](https://img.shields.io/badge/version-v2.1-white?style=flat-square&labelColor=black)](https://github.com/kieranperk/initlife/releases)
[![No Backend](https://img.shields.io/badge/backend-none-white?style=flat-square&labelColor=black)](#)

</div>

---

## `// what`

InitLife is a mobile-first personal dashboard styled as a terminal. No app store, no login required, no backend. Open it, set your name, and it becomes your ambient life display - real-time clock, day/week/year progress, focus windows, and optional Google account sync.

Built to live as a pinned tab on your PC and a home screen shortcut on your phone.

---

## `// features`

```
[✓] real-time clock with live seconds
[✓] day · week · year progress bars with time remaining
[✓] time-aware greeting with your name
[✓] focus window suggestions based on time of day
[✓] custom theme / accent colour picker
[✓] configurable widgets (show/hide sections)
[✓] auto geolocation via nominatim reverse geocoding
[✓] weather api integration (real-time conditions)
[✓] pomodoro / focus timer mode
[✓] google oauth 2.0 - no backend, token stays on device
    ├── google calendar  →  next event this week
    ├── gmail            →  unread count
    └── birthdays        →  upcoming in next 14 days (auto-hides)
[✓] rotating dev/engineering quote log  (↻ to cycle)
[✓] dynamic page title  →  HH:MM · XX% day · InitLife
[✓] installable as PWA  →  android prompt + ios instructions
[✓] session uptime counter
[✓] 100% localStorage  -  all data stays on your device
[✓] single .html file  -  no dependencies, no build step
```

---

## `// stack`

```
html      → structure
css       → monochrome terminal aesthetic (JetBrains Mono · Share Tech Mono)
javascript → vanilla, no frameworks, no bundler
google    → calendar api · gmail api · people api (oauth 2.0 implicit flow)
nominatim → openstreetmap reverse geocoding
```

No npm. No webpack. No React. One file.

---

## `// deploy`

### github pages (recommended)

```bash
git clone https://github.com/kieranperk/initlife.git
cd initlife
# rename initlife.html to index.html, push to main
# enable github pages → settings → pages → deploy from branch
```

Then point your domain DNS to GitHub Pages:

```
Type   Host   Value
A      @      185.199.108.153
A      @      185.199.109.153
A      @      185.199.110.153
A      @      185.199.111.153
CNAME  www    kieranperk.github.io
```

### local

```bash
# just open the file - no server needed for basic features
open initlife.html

# for google oauth to work, serve over https or localhost
npx serve .
```

---

## `// google oauth setup`

Google sync is optional. To enable it:

```
1. console.cloud.google.com  →  new project
2. enable APIs:
   - Google Calendar API
   - Gmail API
   - People API
3. credentials  →  create oauth 2.0 client id  →  web application
4. authorised javascript origins:
   - https://initlife.app
   - http://localhost (for dev)
5. authorised redirect uris:
   - https://initlife.app/
   - http://localhost/initlife.html
6. paste client id into initlife.html → GOOGLE_CLIENT_ID
```

> **note:** the client secret is not needed and should never appear in the frontend.  
> tokens are stored in `localStorage` with expiry tracking. nothing leaves the device.

---

## `// project structure`

```
initlife/
├── index.html      ← the entire app
├── README.md       ← you are here
└── LICENSE         ← mit with commons
```

---

## `// roadmap`

```
[ ] google tasks integration
[ ] offline service worker / full pwa cache
```

---

## `// license`

MIT with Commons Clause - see [`LICENSE`](./LICENSE).

You can use, modify, and share InitLife freely.  
You may **not** sell it or offer it as a paid hosted service without permission.

---

<div align="center">

built by [kieranperk](https://github.com/kieranperk) · [initlife.app](https://initlife.app)

</div>

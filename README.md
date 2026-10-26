# OpenClaw diagnostics

Diagnostic captures shared with the upstream OpenClaw project.

## 2026-10-25: gateway 2026.10.6 main-thread saturation (Windows 11)

These are for [openclaw/openclaw#134993](https://github.com/openclaw/openclaw/issues/134993).

- **What they are:** V8 `.cpuprofile` files, 15 s each, captured from a live gateway through the Node inspector. You can open them in Chrome DevTools → Performance, or in speedscope.
- **What was changed:** file URLs are made package-relative (`<npm-global>/node_modules/...`) and nothing else is altered.

| file | state |
|---|---|
| `gateway-42768-20261025.cpuprofile` | boot with `skills.load.watch` at default: `flushSkillsWatchChanges` → `@openclaw/fs-safe` lstat/realpath |
| `gateway-38928-20261025.cpuprofile` | after a restart with `skills.load.watch: false` |

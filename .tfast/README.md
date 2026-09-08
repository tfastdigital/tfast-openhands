# TFast OpenHands

Independent fork: https://github.com/tfastdigital/tfast-openhands
Original: https://github.com/OpenHands/OpenHands

Customizations belong on `tfast/development`. MIT license and original attribution are preserved. This checkout is Agent Canvas; Python agent-server changes belong in the separate OpenHands software-agent-sdk repository. No TFast controller or social publishing integration is implemented yet.

## Upstream updates

With Git and Node on PATH, commit your work, switch to `tfast/development`, and run:

```powershell
node .tfast/update.mjs --check
node .tfast/update.mjs
```

The helper fetches upstream/main and prepares new changes on a review branch, leaving development unchanged until you merge after testing. It refuses dirty worktrees. Do not force-push updates. This initial clone is shallow; if an older merge base is needed, run `git fetch --unshallow origin` before retrying.

## Development

Node >=22.12 is required; this machine has Node 24.12. Run `npm ci`, then `npm run build`. Upstream verification commands are `npm run lint`, `npm test`, and `npm run build:lib`. Use VS Code to edit this checkout alongside TFast Cline.

The built frontend alone does not execute agents. Follow README.windows.md for the Docker-backed stack, or configure a separate Agent Server. Live agent requests need provider authentication. Keep GitHub release/publishing workflows disabled until configured for the fork.

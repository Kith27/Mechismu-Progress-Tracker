# FSAE EV · Team Progress Tracker

A single-file dashboard with **GitHub as the database** — all tracker data is stored as `data.json` in your repo, committed automatically on every save.

## Quick Deploy

1. Create a new **public** GitHub repo (e.g. `fsae-tracker`)
2. Upload `index.html` and `data.json` to the root
3. Go to **Settings → Pages → Source: main branch, / (root)**
4. Your dashboard is live at `https://<username>.github.io/fsae-tracker/`

## How GitHub Storage Works

- All tracker data lives in `data.json` in your repo
- Every save triggers a GitHub API commit — fully version-controlled
- **Viewers** just open the URL — no login needed, data loads publicly
- **Leads** configure a Personal Access Token (PAT) once via the ⚙ Setup panel

## First-Time Setup (Leads Only)

1. Go to [github.com/settings/tokens/new](https://github.com/settings/tokens/new)
2. Create a **Classic token** with `repo` scope
3. Open the dashboard → click **⚙ GitHub Setup** in the sidebar
4. Enter your username, repo name, token, and a lead password
5. Click **Save & Connect** — it'll test the connection and load data

The token is stored only in **your browser's localStorage** and goes only to the GitHub API.

## Sharing With the Team

- Share the GitHub Pages URL (`https://...github.io/fsae-tracker/`) — viewers see live data with no setup
- Each division lead does the Setup once on their own machine with the PAT

## Changing the Lead Password

Open ⚙ GitHub Setup and update the password field, then Save & Connect.

## Data File

`data.json` in the repo root. Every edit auto-commits with a timestamped message like:
```
tracker: update data 2025-06-20T10:32:00.000Z
```
You can view the full history of all changes in GitHub's commit log.

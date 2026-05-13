# StreamCenter Scraper

Auto-updating sports streaming link scraper.

## Setup on GitHub

### 1. Create new repository
- Go to [github.com/new](https://github.com/new)
- Name it `streamcenter-scraper`
- Make it **Public**

### 2. Upload files
Push these files to your repository:
```
streamcenter.py
utils.py
requirements.txt
.github/workflows/auto-update.yml
```

### 3. Enable GitHub Actions
- Go to repository **Settings** → **Actions** → **General**
- Select **"Allow all actions"**
- Click **Save**

### 4. Trigger first run
- Go to **Actions** tab
- Click **"Auto Update"** workflow
- Click **"Run workflow"** → **"Run workflow"**

## How it works

- Runs every **6 hours** automatically
- Fetches latest streaming links from StreamCenter API
- Commits any changes back to the repository
- You can also run manually from Actions tab

## Files

| File | Description |
|------|-------------|
| `streamcenter.py` | Main scraper module |
| `utils.py` | Utility functions (Cache, Network, Time) |
| `requirements.txt` | Python dependencies |

## Local Setup

```bash
pip install -r requirements.txt
python -c "import asyncio; from streamcenter import scrape; asyncio.run(scrape())"
```
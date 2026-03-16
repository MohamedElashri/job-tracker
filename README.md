# Job Tracker Widget for SiYuan

Track job applications directly inside your SiYuan notes. All data is persisted as a custom attribute (`custom-job-tracker-data`) on the widget block itself — no external database needed.

## Installation

1. Place the `job-tracker/` folder in your workspace's `data/widgets/` directory. (clone the whole repository)
2. In any SiYuan note, type `/widget` and select **Job Tracker**.

## Data storage

Job data is stored using SiYuan's block attribute API (`/api/attr/setBlockAttrs`) on the widget's own block. This means the data travels with your note and is part of SiYuan's sync and backup.

## Configuration

If your SiYuan instance uses an API token (Settings → About → API Token), open `index.html` and set:

```js
const SIYUAN_TOKEN = 'your-token-here';
```

## Features

- Add / edit / delete applications
- Status: Saved → Applied → Interview → Offer → Rejected → Ghosted
- Priority: High / Medium / Low
- Tags, notes, salary, dates, job URL
- Search + filter by status and priority
- Sortable columns
- CSV export
- localStorage fallback when running outside SiYuan

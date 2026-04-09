# CSV Stats Folder

Place exported quiz CSV files in this folder.

The app looks for CSVs in this order:

1. If `stats/index.json` exists, it loads paths listed in `files`.
2. If no manifest exists, it tries to discover CSV files from a server directory listing at `stats/`.

Example:

```json
{
  "files": [
    "stats/quiz_answers_2026-04-07.csv",
    "stats/quiz_answers_2026-04-08.csv"
  ]
}
```

In both cases, the app unions all found files and deduplicates rows by timestamp.

# sync-download

## Usage

```yaml
name: Sync_Download

permissions:
  contents: write
  actions: write

on: 
  workflow_dispatch:
  schedule:
    - cron: '30 0 * * *'

jobs:
  sync_download:
    runs-on: windows-2019
    steps:
      - name: sync-download
        uses: gendloop/sync-download@main
        with:
          token: ${{ secrets.GENDLOOP_ACCESS_TOKEN }}
```


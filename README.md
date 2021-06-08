### Hello. 👋
#### I am a LUA, HTML and CSS developer. Currently, I am learning JavaScript.
![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=faderzz&theme=monokai)
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit (optional)
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      # See action.yml for all options
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          token: ${{ secrets.METRICS_TOKEN }}

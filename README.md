name: Daily HackerNews
on:
  schedule:
  - cron: 0 12 * * *  # Every day at noon

jobs:
  daily_hackernews:
    name: Daily HackerNews
    runs-on: ubuntu-latest
    steps:

    - name: daily-hackernews
      uses: actions/checkout@v1.0
      with:
        chat_id: "Telegram chat id"
        coount: 5
      env:
        TELEGRAM_KEY: ${{ secrets.TELEGRAM_KEY }}

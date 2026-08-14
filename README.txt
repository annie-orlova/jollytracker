JOLLYENGLISH TRACKER — GITHUB SETUP

Files in this package:
- index.html
- .github/workflows/update-sheet.yml

How it works:
Google Sheets -> GitHub Action -> data.csv -> index.html

This avoids browser CORS completely.

SETUP
1. Put index.html in the root of your GitHub repository.
2. Put update-sheet.yml at exactly:
   .github/workflows/update-sheet.yml
3. Commit/push both files.
4. Open the repository -> Actions -> Update tracker data -> Run workflow.
   The action creates data.csv automatically.
5. In Settings -> Pages, publish the repository root from your main branch.

After that GitHub checks the Google Sheet automatically every 5 minutes.
The site reads data.csv from the same repository.

IMPORTANT
- Keep the Google Sheet published to the web.
- You do NOT need to edit index.html when marks change.
- GitHub scheduled workflows can occasionally start a little later than the exact cron time.

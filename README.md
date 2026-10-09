HackerRank: Display missing solved counts
========================================

Some HackerRank contest leaderboards show a blank Score column even
though the number of problems solved is present in the backend data.
These scripts work around the display issue in your browser.

The scripts are attached as plain-text (.txt) files. Open them in a
text editor and copy the code; you do not need to rename the files.

Choose ONE of the methods below. The scripts display problems solved,
not points, and do not change submissions or official rankings.

WAY 1: TAMPERMONKEY / GREASEMONKEY / ANOTHER USERSCRIPT MANAGER

1. Install Tampermonkey from your browser's extension store:

   Chrome:
   https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo

   Firefox:
   https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/

   Safari (App Store; a purchase may be required):
   https://apps.apple.com/us/app/tampermonkey/id6738342400

   You can also use another userscript manager, such as Greasemonkey
   on Firefox. The menu names may differ.

2. Open the extension and choose Create a new script (or equivalent).
   Open the attached hackerrank-userscript.txt in a plain-text
   editor, copy all its contents, and paste them into the extension's
   script editor, replacing all default contents. Save the script.

3. Make sure the script is enabled and the extension is allowed to run
   on www.hackerrank.com. Reload the contest leaderboard.

This method runs automatically on subsequent visits. To stop it,
disable the script in the extension and reload the page.

WAY 2: BROWSER CONSOLE (NO EXTENSION NEEDED)

1. Open the contest leaderboard on www.hackerrank.com while logged in.
2. Open the attached hackerrank-console-script.txt in a plain-text editor and
   copy all of its contents.
3. Open your browser's Developer Tools:
   - Chrome/Edge: Ctrl+Shift+J on Windows/Linux; Cmd+Option+J on Mac.
   - Firefox: Ctrl+Shift+K on Windows/Linux; Cmd+Option+K on Mac.
   Alternatively, use the browser menu to open Developer Tools.
4. Select the Console tab, paste the entire script, and press Enter.
   If your browser shows a paste-protection notice, read it and follow
   its displayed instructions only after reviewing the script.
5. The blank Score cells should now show solved counts.

This method continues working as you change leaderboard pages, but
must be repeated after reloading the page. Reloading also stops it.

WHAT BOTH METHODS DO

- Display problems solved, not points.
- Preserve scores already displayed by HackerRank.
- Fetch leaderboard data from HackerRank using your current session.
- Handle pagination and refresh every minute while the tab is visible.
- Change only your browser display, not submissions or official ranks.

The scripts use the contest name in the page URL. They support the
HackerRank contest leaderboard layout for which this fix was written;
different layouts or future site changes may require an update.

IF NOTHING CHANGES

- Confirm you are on the contest's Leaderboard page and logged in.
- For Way 1, confirm the script and extension site access are enabled.
- If scores already appear, the script intentionally leaves them alone.
- For Way 2, look for a "HackerRank solved-count fix" error in Console
  and share the error text with the organizer. Do not share cookies,
  authorization headers, or other login information.

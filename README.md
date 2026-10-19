# Next Up — user guide (version 1.02)

Next Up tracks the TV shows you're watching and a watchlist of movies. It replaces Twee.
It runs on your phone, works offline, and keeps a live backup in your own Dropbox.

App address: **https://sskehan.github.io/nextup/**

## Files in this repository
index.html · sw.js · manifest.json · icon-192.png · icon-512.png · README.md

Only program files go here. The repository is public, so **never upload a backup file to GitHub.**

## 1. Install on your phone
1. Open the app address in **Chrome**.
2. Tap **⋮ → Add to Home screen** (or **Install app**) → **Install**.
3. Open Next Up from the new icon. It runs full-screen and works offline.

## 2. Load your shows
- **New phone, or cleared Chrome:** tap **Get my shows from Dropbox**, sign in, tap **Allow**. Everything comes back.
- **Starting fresh:** tap **⋮ → Add several shows at once**. Put one show per line, then `|` and how far you're up to:
  - `all` = caught up
  - `S02E08` = watched up to that episode
  - `S01` = finished season 1
  - `none` = not started

  If two shows share a name, add the year in brackets, e.g. `Rake (2010)`.

## 3. Everyday use
- **Shows tab:** each tile shows the next episode to watch. Tap the **✓** on a poster to mark it watched (Undo appears briefly).
- **Sort button** (top bar): A–Z (the default; "The" is ignored), To watch first, Recently watched, or Next air date. Movies sort A–Z, by Recently added, or by Year.
- **Filters:** All, To watch, Caught up, Finished.
- **A show's page:**
  - **Overview** has the Up next card, progress and time left, details and cast.
  - **Episodes** lists seasons newest first. **Tap an episode to read its synopsis.** Tap the eye to mark it watched. Press and hold an eye to mark everything up to that episode. **Watch all** does a whole season.
- **Upcoming tab:** episodes aired this week that you haven't watched, then the next two months by day.
- **Movies tab:** To watch and Watched. Open a movie and tap **Mark as watched**.
  Movie search uses Apple's iTunes catalogue. Films still in cinemas and some streaming originals may be missing. Use **Not listed? Add** to add them by title.
- **Suggested tab (from friends):** tap **+**, type who suggested it and their comment, then search and tap **Save**.
  - You can filter by TV, Movies or friend.
  - **Start watching** / **Add to watchlist** moves it across, and the show or movie page shows who suggested it.
  - **Not for me** removes it (with Undo).
- **Where to watch** on any show or movie opens JustWatch Australia.
- **⋮ → Help** has this guide inside the app.

## 4. Dropbox backup
Set up once: **⋮ → Backup & restore → Connect Dropbox**, sign in, tap **Allow**.

- Next Up can only see its own folder, **Dropbox › Apps › NextUp**:
  - `live/nextup.json` is the current copy, updated a few seconds after every change.
  - `snapshots/` holds one full copy per day, plus one before every restore. Snapshots are kept for 60 days.
- The line under "Next Up" shows the status:
  - **In Dropbox ✓**: everything is saved.
  - **2 changes waiting for Dropbox**: they'll go when you're online.
  - **Not backed up**: Dropbox isn't connected.
- **Backup & restore** has these options: Sync now, Snapshot now, Restore a Dropbox snapshot, Only sync on Wi‑Fi, and Disconnect. It also has a **backup file** option (saves to Downloads) for use without Dropbox.

## 5. Changing phones
1. Install the app on the new phone (step 1).
2. Tap **Get my shows from Dropbox**.

If you later open the app on the old phone, it loads the newer copy from Dropbox instead of overwriting it. If both phones have changes, it asks which copy to keep, and saves the other as a snapshot.

## 6. Clearing Chrome's history
Untick **Cookies and site data**. Ticking it deletes Next Up's data on the phone. Dropbox still has it, but you'll need to connect Dropbox again to get it back.

## 7. Updating the app
1. Upload the changed files to this repository (**Add file → Upload files → Commit changes**).
2. Close the app fully, then reopen it while online.

Your data is not affected. The version number is shown in **⋮** (bottom of the menu) and in **About**.

## Dropbox app settings (for reference)
- Dropbox App Console app: **NextUp** (Scoped access, App folder)
- Permissions: `files.metadata.read`, `files.content.read`, `files.content.write`
- Redirect URI: `https://sskehan.github.io/nextup/`
- Only the App key is built into the app. The App secret is never used.

## Where the information comes from
- TV shows and episodes: TVmaze (free, no account).
- Movies: Apple's public iTunes catalogue.

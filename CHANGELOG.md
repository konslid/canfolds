# Changelog

## v0.9.15-beta

Everything below landed since the first public build. Canfolds is still a
single portable exe with nothing to install, and your layouts still live
in a hidden file next to your own files.

### Canfolds now tells you what it is doing

- **Notification system.** Transfers, deletions, failed operations and
  background jobs all report themselves instead of happening silently.
  Positive messages fade on their own; anything that lost or kept data
  stays on screen until you acknowledge it. The display time for the
  positive ones is configurable in Options.
- **Improved progress for folder copies** — the progress bar moves through the
  whole folder, and the completion message counts the actual files inside
  it instead of saying "1 of 1".
- **Improved captions.** Pixel dimensions are shown only for formats that
  genuinely have them; formats previewed through a system icon no longer
  display that icon's resolution as if it were the file's size.
- Publishing a web gallery announces itself the moment the sync starts,
  not when the first file finally moves.

### Files stay in sync with what you do outside Canfolds

- **Auto-refresh of changed files.** Save a picture in another app and its
  card refreshes itself here — thumbnail and caption both — without
  leaving the folder or pressing Refresh. It keeps working while Canfolds
  is not the active window, so a second monitor shows your latest save.
  Only dates and sizes are checked in the background (every 2 seconds by
  default; interval and on/off switch live in Options), changes are
  applied in batches, and a folder on a slow network share backs itself
  off automatically.
- Pixel dimensions no longer get stuck on an old value after a file has
  been overwritten.

### Reading the canvas

- **Captions rewritten for readability:** the file's data first, the name
  below it, the extension left out of the name (it is already in the data
  line and in the border color), long names wrapped over two lines the
  way Windows 11 desktop labels are, and the full name in a tooltip that
  appears almost instantly. Caption text is bigger by default.
- **Ctrl+wheel** temporarily scales caption text on the canvas you are
  looking at, and forgets it when you leave the folder.
- **Text files get real cards** — `.txt` and `.md` show a readable
  preview built from the shape of their first page.
- **PDF is a first-class format** with a genuine first-page preview and a
  warm page-like backdrop, instead of being hidden behind a filter.

### Canvas and arranging

- **Ctrl+U swaps the two panes** with everything in them: folders, zoom,
  selection, history, even an open document editor.
- **H wraps the selected objects in a comment titled with their names** —
  a one-key way to say "these belong together".
- **Arrange → By source height / width / size** — repositions a selection
  using the file's own real data (the same numbers shown in its caption).
- **By height / width / size / scale on canvas** equalizes the selection
  to the group's own average, with `E` as a one-key alias for width.
- **One-key aliases** for the arrange rows you use most: `1` align left,
  `2` align top, `3` equalize height, `4` equalize size.
- **L** locks and unlocks the selection from the keyboard, **Alt+F2**
  renames the selected object.
- **Middle click** opens a folder, drive or shortcut in the other pane —
  from the canvas or from the tree, un-hiding that pane if needed.

### Drives and navigation

- **Drive overview canvas** — every drive as a card with its own icon by
  type, volume label, free space and a fill bar. Shift+click on Up jumps
  to the root of the current drive; plain Up from there opens the
  overview. Drive cards carry a trimmed menu and cannot be dragged into
  folders.
- **Custom folder icons show on every row that folder appears on** — in
  Favorites, Explorer favs, User folders and Drives alike, in both panes,
  and icons set earlier are picked up on start.
- **Imported Explorer pins are yours to manage** — remove them one by one
  from Canfolds without touching Explorer itself.

### Help and first steps

- **A full PDF manual ships with the app** — the whole program described
  in one document, opened straight from About → Open full PDF help, and
  included in the onboarding tour.
- The web gallery settings page opens with a plain-language explanation of
  what the feature is for (and what it is not).

### Plugins (new, still alpha)

Canfolds now supports plugins: big optional features that install as a
separate file instead of growing the app itself. Four already exist — a
3D model viewer, a diagram editor, an office document viewer/editor, and
browser bookmark management, all working inside Canfolds itself. **They
are alpha and not ready for release, so they are not part of this
download.**

### Fixes

Dozens of bug fixes and stability improvements across file operations,
layouts, previews and the interface, most of them found and reported
during daily use.

## v0.8.3-beta — first public release

Canfolds has been built and used privately for a while before this first
public build. Highlights of what's in this release:

- Dual-pane canvas browser — every folder opens as a freely arranged board
- The layout lives in a hidden per-folder file, never imported into the app
- Scale, 15°-snapped rotation, Z-order, comment frames, markdown notes
- Arrange / Align / Distribute / Normalize, shared anchor across a group
- Video and audio play right on the canvas, with a readable waveform track
- PSD/PSB flattened composite previews
- Built-in 3D preview renderer (FBX/OBJ/STL/GLB/GLTF/PLY), plus
  Blend/Max/ZBrush/Substance viewport previews where available
- Optional web gallery — mirror a folder to your own FTP/web hosting as a
  small, password-protected page, browsable from any device
- Automatic layout backups (20 revisions) and undo for canvas + file
  operations
- Portable — single exe, nothing to install
- 9-language interface (English, Russian, German, Spanish, French,
  Portuguese, Chinese, Japanese, Korean), switches instantly, no restart

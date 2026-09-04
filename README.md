# Daily Manna — audio

Narrated articles for [daily-manna](https://github.com/PolarStellar/daily-manna),
served over GitHub Pages at
`https://polarstellar.github.io/daily-manna-audio/<date>/<rank>.mp3`.

They live here rather than in the main repo because MP3s are the only thing that
grows by megabytes a day, and in-tree every one ever rendered stayed in git
history forever. Keeping them here leaves the reader's repo small while the
audio stays streamable.

They are **not** in GitHub Releases, which was tried first and cannot work:
release downloads are served `Content-Type: application/octet-stream` with
`Content-Disposition: attachment` — hardcoded into the signed URL — and Safari
refuses to play audio on those. Pages sends `audio/mpeg` and supports byte
ranges, which is what the player needs to start and to seek.

Old narration is pruned after 30 days by the main repo's generator. This repo's
history is disposable: nothing here cannot be re-rendered, so if it ever gets
too large it can be recreated from scratch.

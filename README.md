# osm-carto-fonts

Unmodified, byte-identical copies of the files that
[openstreetmap-carto](https://github.com/openstreetmap-carto/openstreetmap-carto)'s
`scripts/get-fonts.py` downloads. This gives the script a download source that
doesn't disappear when an upstream host does (for example openstreetmap-carto#5331).

Paths mirror the upstream layout:

| Path | Upstream | Version |
|---|---|---|
| `noto-fonts/` | https://github.com/notofonts/noto-fonts (archived) | `main` = ffebf8c1ee449e544955a7e813c54f9b73848eac |
| `noto-cjk/` | https://github.com/notofonts/noto-cjk | `main` = f8d157532fbfaeda587e826d4cd5b21a49186f7c (the JP OTFs last changed in 165c01b4, 2021) |
| `noto-emoji/Noto_Emoji.zip` | https://archive.org/download/noto-emoji/Noto_Emoji.zip | as of 2026-10-31 |
| `hanazono-font/68253/hanazono-20170904.zip` | `https://mirrors.dotsrc.org/osdn/hanazono-font/68253/hanazono-20170904.zip` (gone), taken from Wayback capture 20260811045230 | HanaMinA/B inside are byte-identical to the copies get-fonts.py installed from the live mirror in May 2026 |

`SHA256SUMS` covers every file (`sha256sum -c SHA256SUMS`).
The same hashes apply to the upstream sources, so a client can pin hashes and still treat
this repo and upstream as interchangeable.

Link to files with a commit SHA, not a branch name:
`https://raw.githubusercontent.com/leijurv/osm-carto-fonts/<commit>/<path>`.

## Licenses

The fonts keep their own licenses, and the license text ships next to them:
SIL Open Font License 1.1 (`noto-fonts/LICENSE`, `noto-cjk/Sans/LICENSE`, `OFL.txt` inside the emoji zip),
and Hanazono Font License / OFL 1.1 dual license (`LICENSE.txt` inside the Hanazono zip).

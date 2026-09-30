# 📚 AppShelf sources

[Русский](README.ru.md) · **English**

A catalog of alternative download links for Android apps — GitHub releases, Telegram channels,
project sites — used by [AppShelf](https://github.com/Xtratter/appshelf) when you set up a new phone.

AppShelf downloads [`sources.json`](sources.json) as a whole (at most once a day), so nothing about your
installed apps is sent anywhere. Links you add yourself in AppShelf always come first; links from this catalog
are shown after them.

## Format

```json
{
  "format": "AppShelf-sources",
  "version": 1,
  "apps": {
    "<package name>": [
      { "url": "https://github.com/owner/repo", "label": "GitHub" },
      { "url": "https://t.me/channel", "label": "Telegram" }
    ]
  }
}
```

- The key is the app's package name (AppShelf shows it in the app card and can copy it).
- `url` — any `https://` link: a GitHub / GitLab / Codeberg repository (AppShelf opens its latest release and can add it to Obtainium),
  a Telegram channel, a forum thread, a site or a direct `.apk` link.
- `label` is optional — without it AppShelf names the link by its site.

## Adding links

In AppShelf add links in the app cards, then **Save & export → Links for the catalog** gives you a ready `sources.json`
with all your links — merge it here. Pull requests are welcome.

## Use your own catalog

Fork this repository and set the address of your `sources.json` in AppShelf (menu → Link catalog).
Any `https://` address that serves this format works.

## License

[CC0 1.0](LICENSE) — the list of links is in the public domain.

# Graphite: a calm light theme for Mailspring

A light theme for [Mailspring](https://getmailspring.com) built around a charcoal sidebar, airy three-line message cards and the [Inter](https://rsms.me/inter/) typeface. Every size comes from one measured layout grid.

Pairs with three small plugins, each installable on its own:

- **[mailspring-plugin-avatars](https://github.com/jblavisse/mailspring-plugin-avatars)**: sender avatars in the thread list.
- **[mailspring-plugin-list-header](https://github.com/jblavisse/mailspring-plugin-list-header)**: folder name and a compose button above the list.
- **[mailspring-plugin-draft-cards](https://github.com/jblavisse/mailspring-plugin-draft-cards)**: the Drafts folder as inbox-style cards.

## What changes

| Area | Graphite |
|---|---|
| Sidebar | Charcoal `#26272b`, white labels, selected folder as a blue rounded pill, 35px rows |
| Thread list | Always three-line cards (sender · subject · preview), 78px rows, white background for read and unread mail, no row rules |
| Typography | Inter everywhere: interface, composer text, plain-text emails |
| Toolbar | Bare icons with a hover fill, no outlined pills, no hairline across the sidebar |
| Search | Filled rounded field, 16px from the column edges |
| Reading pane | Light grey surface, each message on a white card (12px radius, 16px inset), 20px subject |
| Replies | "Write a reply…" as its own card; inline reply composer on white with a rounded focus ring |
| Composer | Shared 24px margins, prominent subject, flat blue **Send** button |

Spacing scale: 4 · 8 · 12 · 16 · 24 px. Secondary text meets WCAG AA contrast (4.9:1 on white).

## Requirements

- Mailspring **1.26** or later. The toolbar rules target the macOS 26 toolbar introduced in 1.26.
- The **Inter** font, recommended. Without it Graphite falls back to the system font.
  - macOS: `brew install --cask font-inter`
  - Other systems: download from [rsms.me/inter](https://rsms.me/inter/)

## Install

**From a ZIP**

1. Download this repository (Code → Download ZIP) and unzip it.
2. In Mailspring: **Mailspring → Install Theme…**, then pick the unzipped folder.
3. Select **Graphite** in **Mailspring → Change Theme…**

**From Git (to follow updates)**

```bash
git clone https://github.com/jblavisse/mailspring-theme-graphite.git
```

Link it into Mailspring's packages folder (macOS path shown; on Linux use `~/.config/Mailspring/packages`):

```bash
ln -s "$PWD/mailspring-theme-graphite" "$HOME/Library/Application Support/Mailspring/packages/mailspring-theme-graphite"
```

Restart Mailspring, then pick **Graphite** in **Change Theme…**

## Recommended settings

- **View → Reading Pane Vertical**, then drag the list to about 510px wide.
- Install the three companion plugins listed above.

## Limitations

- Light only: no dark variant yet, and the accent is a fixed blue that ignores the system accent color.
- Tuned and tested on macOS. Windows and Linux should work, but the toolbar rules were written for macOS.
- Some rules use `!important` because Mailspring's macOS toolbar and send-button styles otherwise take precedence. Each one is commented in `styles/graphite.less`.
- The theme depends on Mailspring's class names; a future Mailspring release may need small adjustments.

## Uninstall

**Mailspring → Change Theme…**, pick another theme, then delete the `mailspring-theme-graphite` folder from Mailspring's packages folder.

## Credits

Layout proportions were measured from today's polished mail clients, including Spark Desktop. Graphite is an independent project, not affiliated with Readdle or Foundry 376.

## License

[GPL-3.0-or-later](LICENSE), the same license as Mailspring.

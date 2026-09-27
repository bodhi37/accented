# Accented

A lightweight theme for [Spicetify](https://github.com/spicetify) that replaces Spotify's green with a color of your choice.

![preview](./img/preview.png)

> [!NOTE]
> Maintained fork of https://github.com/JWWolstenholme/accented at [a36d969](https://github.com/JWWolstenholme/accented/commit/a36d96948dbff6629b5253913b5b028e3b630437) (itself a fork of https://github.com/updxg/accented at [576f539](https://github.com/updxg/accented/commit/576f539a8e9099e1e8bad137b19f47fd52fb1c51)). Kept detached from the fork network so it shows up in Spicetify Marketplace searches, which skip forks.

This theme was originally created by [@luximus-hunter](https://github.com/luximus-hunter) in Feb of 2022, kept alive by [@updxg](https://github.com/updxg)'s fork (among others) after it was deleted, then brought back to the marketplace by [@JWWolstenholme](https://github.com/JWWolstenholme). This fork picks it up from there and fixes the accent colour leaking over the whole window.

## Color options

- Red
- Orange
- Yellow
- Green
- Blue
- Purple
- Magenta
- Pink
- White
- Full White (also hearts)

## Installation

**Spicetify Marketplace** (recommended)

Install the theme though the [Spicetify Marketplace](https://github.com/spicetify/marketplace). This will allow you to change the color quickly in-app.

![colors](./img/colors.png)

**Linux and MacOS** in Bash:

```bash
cd "$(dirname "$(spicetify -c)")/Themes"
git clone https://github.com/bodhi37/accented
spicetify config current_theme accented
spicetify config color_scheme <color scheme name>
spicetify apply
```

**Windows** in Powershell:

```powershell
cd "$(spicetify -c | Split-Path)\Themes"
git clone https://github.com/bodhi37/accented
spicetify config current_theme accented
spicetify config color_scheme <color scheme name>
spicetify apply
```

## Development

1. Install and activate the theme manually (not via the marketplace) with the instructions above
1. Install [npm](https://www.npmjs.com/)
1. Install [sass](https://sass-lang.com/): `npm install -g sass`
1. Run `spicetify watch -s` to reload spotify when `user.css` is modified
1. Edit [`user.scss`](/user.scss). **Not** `user.css`
1. Run `sass --no-source-map user.scss:user.css` to compile and output to the [`user.css`](/user.css) file

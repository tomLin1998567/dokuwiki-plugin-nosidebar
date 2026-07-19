# DokuWiki Plugin: NoSidebar — PHP 8 Compatible Fork

Fork of [Lupo49/dokuwiki-plugin-nosidebar](https://github.com/Lupo49/dokuwiki-plugin-nosidebar) (unmaintained, last updated 2013).

Allows hiding the sidebar on individual pages via the `~~NOSIDEBAR~~` syntax.

## ✅ PHP 8 Compatibility Fix

The upstream plugin triggers a deprecation warning under PHP 8 due to an outdated `require_once()`. This fork removes it — modern DokuWiki uses autoloading instead.

| Fix | Before | After |
|-----|--------|-------|
| Remove `require_once` | `require_once(DOKU_PLUGIN.'action.php')` | Removed (autoloading) |

No functionality changes.

## Installation

```bash
cd /path/to/dokuwiki
git clone https://github.com/tomLin1998567/dokuwiki-plugin-nosidebar.git lib/plugins/nosidebar
```

Or download the ZIP from the [releases page](https://github.com/tomLin1998567/dokuwiki-plugin-nosidebar/releases).

Then enable the plugin via **Admin → Extensions**.

## Usage

Add `~~NOSIDEBAR~~` anywhere on a page to hide the sidebar for that page.

## Credits

- Original author: [Matthias Schulte](https://github.com/Lupo49)
- PHP 8 compatibility fix by [tomLin1998567](https://github.com/tomLin1998567)

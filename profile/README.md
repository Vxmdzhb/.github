<h1 align="center">AstrX</h1>

<p align="center">
  <b>Your own corner of the internet: forum, chat, wiki, mail and search engines,<br>
  in one self-hosted site that works with JavaScript switched off.</b>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Vxmdzhb/astrx/main/docs/screenshots/home.png" width="49%" alt="AstrX home page">
  <img src="https://raw.githubusercontent.com/Vxmdzhb/astrx/main/docs/screenshots/chat.png" width="49%" alt="AstrX chat">
</p>

Most of the web now needs a megabyte of script before it shows you a sentence.
AstrX goes the other way. Every page is plain HTML rendered on the server, so it
loads in an instant, works in any browser, and runs happily in Tor Browser on
its safest setting. Put it behind an onion address and you have a community
space that needs nothing from anyone else.

## What you get

- **A chat** with rooms, private messages and moderation, refreshing itself
  without a single line of script.
- **An imageboard** with threads, images, greentext, catalogs and the
  classic board styles.
- **A wiki**: Markdown pages with `[[links]]`, backlinks and a page graph.
- **Webmail**, an **anonymous tip line** sealed with public-key crypto, a
  **warrant canary**, signed downloads and mirror lists.
- **Search engines you own.** Not a front end for someone else's API: real
  crawlers and indexes for the clear web, for onion services and for the
  BitTorrent DHT, written in Rust and running on your machine.
- **Ten themes**, from black-and-white to amber terminal to synthwave. Each
  visitor picks their own.

## Built to be trusted

- **No JavaScript anywhere.** No trackers, no CDNs, no fonts from someone
  else's server. A strict Content-Security-Policy on every page.
- **No third-party PHP packages.** The whole site runs on its own code.
- **No dependencies in the Rust engines by default**: the standard library
  only. Networking adds two well-known crates, and CI checks that it stays that
  way.
- **Small, separable pieces.** The framework, the CMS and every feature are
  their own packages. Switch a module off and it's gone from the site; use the
  framework without the site at all.

## Try it

```sh
git clone https://github.com/Vxmdzhb/astrx.git
git clone https://github.com/Vxmdzhb/astrx-suite.git   # the search engines (optional)
cd astrx && composer install && php tools/install.php
php -S 127.0.0.1:8080 -t public public/index.php
```

Or bring up the site, the engines and Tor in a few containers with
`docker compose up -d`. The [AstrX README](https://github.com/Vxmdzhb/astrx)
has the details.

## The repositories

| | |
|---|---|
| [**astrx**](https://github.com/Vxmdzhb/astrx) | The website. Start here. |
| [**astrx-suite**](https://github.com/Vxmdzhb/astrx-suite) | The Rust engines as one `astrx` binary, with the Docker and Tor setup. |
| [framework](https://github.com/Vxmdzhb/framework) · [library](https://github.com/Vxmdzhb/library) · [cms](https://github.com/Vxmdzhb/cms) | The PHP packages the site is built from. |
| `module-*` | One feature each: [chat](https://github.com/Vxmdzhb/module-chat), [imageboard](https://github.com/Vxmdzhb/module-imageboard), [content](https://github.com/Vxmdzhb/module-content), [webmail](https://github.com/Vxmdzhb/module-webmail), [tipline](https://github.com/Vxmdzhb/module-tipline), [search](https://github.com/Vxmdzhb/module-search) and more. |
| [websearch](https://github.com/Vxmdzhb/websearch) · [onioncrawler](https://github.com/Vxmdzhb/onioncrawler) · [torrentds](https://github.com/Vxmdzhb/torrentds) · [gitweb](https://github.com/Vxmdzhb/gitweb) · [suitedash](https://github.com/Vxmdzhb/suitedash) · [crawlcore](https://github.com/Vxmdzhb/crawlcore) | The Rust engines and their shared library. |

<p align="center">
  <img src="https://raw.githubusercontent.com/Vxmdzhb/astrx/main/docs/screenshots/themes.png" alt="The same page in six of the bundled themes">
</p>

Found a bug, have an idea, or want to help? Issues and pull requests are
welcome in any of the repositories. Security problems: please report them
privately, through the repository's **Security** tab.

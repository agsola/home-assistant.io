[![Discord](https://img.shields.io/discord/330944238910963714.svg)](https://discord.gg/CxqDrfU)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

[![Deploys by netlify](https://www.netlify.com/img/global/badges/netlify-color-bg.svg)](https://www.netlify.com)

# Home Assistant website

This is the source for the [Home-Assistant.io website](https://home-assistant.io).

## Setup

Setting up to contribute to documentation and the process for submitting pull requests is explained in the [developer documentation](https://developers.home-assistant.io/docs/documentation_index.html).

## Site preview

In order to make the preview available on [http://127.0.0.1:4000](http://127.0.0.1:4000), use the command as follows:

```bash
bundle exec rake preview
```

## Speeding up site generation

Every release we post long changelogs to the website. This slows down generation of the website significantly! We include some tools to temporarily exclude the blog posts that you're not working on out of the way.

```bash
bundle exec rake isolate[filename-of-blogpost]
```

When you're done working on the site, run the following command to move the posts back again:

```bash
bundle exec rake integrate
```

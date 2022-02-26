---
title: JSON
description: Enabling the JSON data format
docs: plugins/json.ts/~/Options
enabled: true
tags:
  - data_format
---

${toc}

## Installation

This plugin is installed by default. 🎉

## Configuration

If you want to change the default configuration, use the second argument of
`lume()` function in your `_config.ts` file. See all configuration options by
clicking in the "See available Options in Deno Doc" button above.

```js
import lume from "lume/mod.ts";

// JSON plugin configuration
const json = {
  pagesExtensions: [".page.json"],
};

const site = lume({}, { json });

export default site;
```

## Description

This plugins allows to create pages and store data using the JSON format.

### Create pages

Create a file with the extension `.tmpl.json` in your `src` folder. For example:

```json
{
  "title": "Welcome to my page",
  "layout": "layouts/main.njk",
  "content": "This is my first post using lume,\nI hope you like it!"
}
```

### Create data files

Create a file with the name `_data.json` or inside a `_data` directory.
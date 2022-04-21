+++
title = "Installation and configuration"
description = "How to use this theme"
weight = 1

[extra]
illus = "illus.avif"
+++

Create your Zola site, and import this theme:

```bash
zola init NAME
cd NAME/themes
git clone https://github.com/elegaanz/zola-theme-course.git
cd ..
```

Then update your `config.toml` with this line:

```toml
theme = "zola-theme-course"
```

You can also add these lines to customize how the theme behaves:

```toml
[extra]
site_name = "My course"
icon = "image.png"
icon_desc = "Icon of the course"
description = "A great course!"
default_illus = "illus.png"
primary_color = "#FFFFFF"
accent_color = "#FFFFFF"
source_url = "https://github.com/me/my-course"
```

## File structure

For your course to be displayed correctly, it needs to follow a specific structure.

- `content/_index.md` is the text displayed on the homepage
- each part should have its own folder, with an `_index.md`
- each subpart should have its own markdown file (which can be an `index.md` in a subfolder)
- all `_index.md` files should have `sort_by = "weight"` in their frontmatter, and you can then
  order parts and subparts using the `weight` option.

With this theme, pages can also have extra options:

```toml
[extra]
# Don't display the page title, useful for the homepage
no_title = true
# The name of the image to use as a banner
illus = "illus.jpg"
# Adds JSON-LD metadata on this page, useful for the homepage
jsonld = true
```

The standard `title` and `description` fields are also taken into account.
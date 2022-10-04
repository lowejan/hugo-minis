---
title: About Hugo Minis
author: Wejan
---

**Minis** is a Hugo theme written by [Wejan](https://wejan.cn), it's modified from Yihui's [XMin](https://github.com/yihui/hugo-xmin/) theme, most of `contents` and `styles` are from xmin. The main motivation for writing this theme was to provide a simple and minimal theme for myself. Here is my website as a [demo](https://wejan.cn)(Chinese).

# config.toml

For this example site, I defined permalinks for sections `post`, so that the links to pages under the directory will contain the date info, e.g., `https://minis.wejan.cn/post/2016/02/14/a-plain-markdown-post/`. This is optional, and it is up to your personal taste of URLs.

```toml
permalinks:
  post = "/post/:year/:month/:day/:slug/"
```

You can define the menu through `menu.main`, e.g.,

```toml
[[menu.main]]
    name = "Home"
    url = ""
    weight = 1
[[menu.main]]
    name = "About"
    url = "about/"
    weight = 2
[[menu.main]]
    name = "Categories"
    url = "categories/"
    weight = 3
[[menu.main]]
    name = "Tags"
    url = "tags/"
    weight = 4
[[menu.main]]
    name = "Subscribe"
    url = "index.xml"
```

Alternatively, you can add `menu: main` to the YAML metadata of any of your pages, so that these pages will appear in the menu.

The page footer can be defined in `.Params.footer`, and the text is treated as Markdown, e.g.,

```
params:
  footer = "&copy; 2022 -- {Year} [Wejan](https://wejan.cn)"
```

Here `{Year}` means the year in which the site is built (usually the current year).

## LaTeX math expressions support

It can easily support LaTeX math expressions, using [Yihui's solution](https://yihui.org/en/2018/07/latex-math-markdown/), With a little bit customization, e.g.,

`$${\sqrt {n}}\left(\left({\frac {1}{n}}\sum _{i=1}^{n}X_{i}\right)-\mu \right)\ {\xrightarrow {d}}\ N\left(0,\sigma ^{2}\right)$$`


The source code is [on Github](https://github.com/lowejan/hugo-minis). Happy hacking!

+++
title = "Sample Post: Hello, Hugo"
date = '2026-09-12'
draft = false
tags = ["meta", "hugo"]
summary = "Placeholder post used to verify the Hugo + PaperMod setup. Replace or delete it once you start writing."
+++

> **This is a sample/test post.** It exists so the freshly initialized site has
> one page that exercises headings, prose, links, and a code block. Delete it
> (and this file) when you publish your first real article.

## Why this post exists

The repository was bootstrapped with [Hugo](https://gohugo.io/) and the
[PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. This page is a
smoke test for the rendering pipeline: front matter, Markdown, syntax
highlighting, table of contents, and reading time.

### What to check on this page

1. The table of contents is generated from the headings below.
2. Reading time appears under the post title.
3. The code block has a **copy** button in its corner.
4. Tags at the bottom link to the `tags` taxonomy.

## A code block

PaperMod highlights fenced code blocks with class-based Chroma styles:

```python
from dataclasses import dataclass


@dataclass(frozen=True)
class Post:
    title: str
    tags: tuple[str, ...]

    def summary(self) -> str:
        return f"{self.title} [{', '.join(self.tags)}]"


print(Post("Hello, Hugo", ("meta", "hugo")).summary())
```

Shell commands work the same way:

```bash
# Build the site for production
hugo --gc --minify
```

## Working with the site locally

Start the development server with drafts enabled:

```bash
hugo server -D
```

Then edit files under `content/` and the browser reloads automatically. When you
are ready to publish, commit and push — the production build is generated with
`hugo --gc --minify`.

## Next steps

- Replace the placeholder `title`, `description`, and social links in `hugo.toml`.
- Write a real first post under `content/posts/`.
- Delete this sample post when it is no longer needed.

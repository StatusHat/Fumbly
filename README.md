# Hugo Fumbly

## Minimal and dumb

**Fumbly** is a Hugo theme made from scratch for me, by me. This is a project where I try to learn something about CSS and Hugo templating.

It doesn't do much. It has a top nav-bar featuring a "posts archive", "tags page" and an "about page". It has a frontpage featuring the three latest posts. It has pagination (older/newer) on the frontpage, the posts archive and each post. Also a footer.

## Configuration

Currently you want to set something like the following in your `config.yaml`:

```yaml
paginate: 3

params:
  footer: "Whatever you want to sit at the bottom of your site at all times"
```

If you like to add some copyright-stuff in the footer, the template translates `{Year}` to current year for you.

You will also want the following files/folders in your `{hugosite}/content/` directory:

```
_index.md
about/
about/index.md
posts/
```

This theme makes use of just a teeny bit of frontmatter ("draft: (true/false)" and other Hugo "behind the scenes" built-ins still work, of course):

- title: (string)
- date: (timedate)
- tags: (list)

## Styling (not necessarily style)

Aiming for simple, non-intrusive and non-ugly. Some might argue I missed that last goal.

## Not very big

Curently 271 lines of code - excluding the included normalize.css.

```bash
$ find . -not -path '*/normalize/*' \( -name '*.html' -o -name '*.css' \) | xargs wc -l
  54 ./layouts/index.html
  10 ./layouts/_default/single.html
  13 ./layouts/_default/baseof.html
  16 ./layouts/_default/list.html
   0 ./layouts/404.html
  35 ./layouts/posts/single.html
  20 ./layouts/posts/list.html
   8 ./layouts/partials/footer.html
  17 ./layouts/partials/header.html
   2 ./layouts/partials/head.html
  96 ./static/css/style.css
 271 total
```

## TODO

- Add a nice custom 404-page
- Add mobile friendliness/responsiveness
- Maybe choose som specific fonts
- Light/dark theme

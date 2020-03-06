# volkamerlab.org

Contents for this website, built with Hugo, a static site generator, and deployed to netlify.com.

This website is based on the [HTML5 Editorial](https://html5up.net/editorial) template.

## Request changes

1. Fork and create a branch on your fork.
2. Install `hugo` from package file on GitHub ([v0.65.3](https://github.com/gohugoio/hugo/releases/tag/v0.65.3)).
   - Ubuntu: `hugo_extended_0.65.3_Linux-64bit.deb`
   - Windows: `hugo_extended_0.65.3_Windows-64bit.zip`
   - macOS: `hugo_extended_0.65.3_macOS-64bit.tar.gz`
3. Run `hugo serve` on this directory while editing. It will autoreload changes on `localhost:1313`.
4. Add, commit, push and submit PR. Netlify will create a deploy preview for you on the PR.
5. Wait for review.


## Where to look for modifications

### Menu

- __Welcome__: `content/_index.md`
- __Research__: `content/research/_index.md/`. Subitems in the menu are in the corresponding `*.md` files.
- __The team__: `content/team/_index.md` (intro text) + `data/team/team.yaml` (member info). Almost everything is encoded in the YAML file. Adding more members is a matter of editing the lists. Responsible code for orchestrating the layout is in `layouts/section/team.html`; each individual member is rendered through `layouts/partials/person.html`.
- __Publications__: This link is harcoded in `partials/menu.html`

### Get in touch

Hardcoded in `partials/contact.html`

### Copyright

Hardcoded in `partials/sidebar_footer.html`

### Header bar

Where the social icons are listed on the right. This part is hardcoded in `partials/topbar.html`.


## Adding pages to the menu

After creating a new `*.md` file in `content/`, you can add it to the menu by specifying this metadata in the YAML header:

```
menu: "main"
```

If the default ordering is not suitable, it can be overriden with a weight:

```
weight: 10
```

Nested submenus must specify the parent too:

```
menu:
    main:
        parent: Research
```

## Resources

### Content management 

* HTML5 Editorial [sample content](https://html5up.net/uploads/demos/editorial/elements.html): Check out content options.
* Hugo [shortcodes](https://gohugo.io/content-management/shortcodes/): Use shortcodes instead of HTML in markdown content.

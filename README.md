# nuxt-path-encoding

Illustrates a Nuxt bug.

## Significant code

- [pages/_slug.vue](pages/_slug.vue)
- A nuxt-link on [pages/index.vue](pages/index.vue) links to the slug page with a non-ascii slug

## Reproduction

1. `yarn generate`
2. Serve `dist` folder: `http-server dist`
3. Visit `/`, click the link, it loads fine
4. Refresh on the slug page

Expected outcome: The page content (a h1 heading) will show

Actual outcome: The page content flashes but disappears

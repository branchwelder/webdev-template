# Template Project

View the deployed template [here](http://twigg.gg/webdev-template/).

This template project uses `vite` to run a dev server and build the project. It
uses `gh-pages` to deploy the site to the `gh-pages` branch.

## Using the template

Clone the repository to your computer and Open it in your editor.

Install dependencies with `npm install`

- `npm run start` - runs the local development server
- `npm run host` - runs the local development server, but makes it accessible on
  your network (so you could e.g. open the site on your phone)
- `npm run build` - builds your site to the `dist` folder
- `npm run preview` - builds your site and previews the built version locally
- `npm run deploy` - builds your site and then deploys it to github pages

**IMPORTANT:** When you want to deploy your site, you will need to update the
path in the deploy script to reflect the name of your repository. This is
because github pages projects are automatically given a subfolder on your base
`username.github.io` domain. For example, this repo is named `webdev-template`,
so the deploy script sets the base path like this:

```json
    "deploy": "vite build --base=/webdev-template/ && gh-pages -d dist"
```

If your repo was instead named `my-cool-project`, you should edit the deploy
script to be:

```json
    "deploy": "vite build --base=/my-cool-project/ && gh-pages -d dist"
```

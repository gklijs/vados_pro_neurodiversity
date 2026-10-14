# PRO Neurodiversiteit

A static site built with [vados](https://github.com/gklijs/vados), scaffolded by `vados init`.

## Content

- `root/` -- the source tree: `main.json`, `menu.json`, and one `page.json` per page directory.
- `imgroot/` -- the image tree: one `images.json` per directory of images to publish.
- `sass/main.scss` -- overrides Bulma's `$primary` before importing it; rebuilt by `npm run build` into `public/css/main.min.css`.

## Local development

```
cargo install vados
npm install
npm run build
vados check --source root --img-source imgroot
vados generate --source root --img-source imgroot --destination public
```

## Deployment

This project deploys to [Netlify](https://www.netlify.com/) with no further setup: connect the repository and `netlify.toml` takes care of installing Rust, `vados`, and the Sass build.

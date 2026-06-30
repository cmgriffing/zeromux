# ZeroMux Satirical Site

ZeroMux is a one-page satirical product site for a fictional terminal
"anti-multiplexer." The joke is that it promises productivity by refusing to do
the things terminal multiplexers are normally useful for: split panes, multiple
windows, configuration, and context switching.

The site is intentionally static. There is no build pipeline, package manager,
or app runtime in this directory.

## Running Locally

Open `index.html` directly in a browser.

For a local server, any static file server works:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## What Is Included

- A dark, developer-tool-style landing page for the fictional ZeroMux product.
- CDN-loaded Tailwind CSS with inline theme configuration.
- Google Fonts and Font Awesome icons loaded from public CDNs.
- Open Graph and Twitter Card metadata with a static PNG preview image.
- Inline CSS for the custom background, glass panels, scrollbars, terminal
  mockup, and joke modal.
- A small inline script that opens and closes the satire disclaimer modal.

## Content Model

The page is structured like a real SaaS/product landing page, but every claim is
part of the parody:

- Hero section for "The Anti-Multiplexer."
- Fake feature cards that frame missing functionality as product value.
- A mock configuration file that cannot be configured.
- Joke testimonials and comparison table.
- FAQ that makes the satire explicit.
- Install CTA that shows a fake `curl | bash` command.

The fake install flow is deliberately intercepted by a modal explaining that
ZeroMux is not real software. Keep that safety guard in place if you edit the
CTA, copy button, or install command.

## Editing Guidelines

- Preserve the core premise: ZeroMux is fake, satirical, and should not be
  presented as installable software.
- Keep the disclaimer visible near the install section and in the modal.
- Do not add a real installer, executable script, package manifest, or download
  link unless the project stops being satire.
- Keep external dependencies CDN-based unless the project gains a real build
  process.
- Edit `og-image.svg` first, then regenerate `og-image.png` from it when the
  social preview artwork changes.
- Treat placeholder social/legal/resource links as part of the joke unless they
  are intentionally replaced with real project pages.

## Deployment

Deploy the directory as static files. A static host such as GitHub Pages,
Netlify, Vercel static output, or any basic web server is sufficient.

No environment variables or server-side routes are required.

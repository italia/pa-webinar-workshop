# PA Webinar workshops

Pages for the hands-on workshops on [PA Webinar](https://github.com/italia/pa-webinar), the open source webinar platform for the Italian public administration.

Published at **https://workshop.pa-webinar.innovazione.gov.it**.

## Layout

- `site/` is the published site, plain HTML and CSS with no build step.
- `site/<event>/index.html` is the page of one workshop, for example `site/sfscon-2026/`. To add a workshop, copy an existing folder and add a card to `site/index.html`.
- `site/assets/` holds the stylesheet and the fonts. Everything is served from the same host: no CDN, no cookies, no analytics.

## How it is served

An nginx container serves `site/`, and a git-sync sidecar pulls this repository every minute. A push to `main` is live within about a minute, with no build and no deploy.

Once a workshop page is printed or shared, for example as a QR code, keep its address: change the content, not the folder name.

## Licenses

- Content: [CC BY-SA 4.0](LICENSE).
- Fonts in `site/assets/fonts/`: Titillium Web and Roboto Mono, under the SIL Open Font License 1.1 ([OFL.txt](site/assets/fonts/OFL.txt)).

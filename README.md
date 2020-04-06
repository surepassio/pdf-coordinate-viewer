## PDF coordinate viewer

This is a very simple fork of the [PDF.js viewer][] that adds the
page coordinates, in [point units][], of the current mouse position
at the bottom-left of the viewport.

It assumes the pages being viewed have [US Letter][] dimensions.

The only changes to the original viewer are in
[`web/viewer.html`](web/viewer.html), which adds links to the following
new files:

* [`web/bookmarklet.css`](web/bookmarklet.css), which contains styling
  for the overlay.
* [`web/bookmarklet.js`](web/bookmarklet.js), which contains the
  overlay functionality. Don't modify this file directly, as it is
  automatically generated from TypeScript source; instead, see the
  instructions below.

## Modifying the functionality

To modify the overlay functionality, install yarn and start
the file watcher:

```
yarn
yarn watch
```

You'll also want to start a web server that serves static files.
For instance, if you have Python 3, this can be done via
`python3 -m http.server`.

Then edit [`bookmarklet.ts`](./bookmarklet.ts). To view your
changes, reload `web/viewer.html` in your browser.

You can also run `yarn build` to rebuild the JS manually.

[PDF.js viewer]: https://mozilla.github.io/pdf.js/getting_started/#download
[point units]: https://en.wikipedia.org/wiki/Point_(typography)
[US Letter]: https://en.wikipedia.org/wiki/Letter_(paper_size)

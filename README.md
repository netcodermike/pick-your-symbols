# Pick Your Symbols

Find a full transversal using exactly the symbols you request.

[Open the web app](https://surfingcoder.com/apps/pick-your-symbols/)

![The app running with its sample input](docs/demo.webp)

## Run locally

Serve the repository with Python 3, then open http://127.0.0.1:8000/ in a current browser.

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Start with the provided example. Adjust the controls and select **Update** to recompute. Sliders refresh the result as you move them.

## Method

The search assigns at most one cell per row, with unique columns and symbols. A full witness proves feasibility. Exhausting the search proves infeasibility for that board and target set.

Inspired by Michael John Harris’s graduate proseminar, *On the Existence of Transversals in r-Multi Latin Squares* (2012).

## Verify

Run `node --test check.mjs` with Node.js 22 or newer. The check runs the app’s mathematical regression cases without a browser.

# Mushfiqur Rahman — Projects Portfolio

[projects.mushfiqr.com](https://projects.mushfiqr.com) is a collection of small web projects, interactive experiments, and utility prototypes by [Mushfiqur Rahman](https://github.com/snick-m). Each project is self-contained and can be opened directly from the portfolio.

## Featured projects

- [Task Generator](https://projects.mushfiqr.com/TaskGenerator) — generate tasks from a configurable list.
- [Random Quote](https://projects.mushfiqr.com/RandomQuote) — display a random quote.
- [Pi Image](https://projects.mushfiqr.com/PImage) — image-based experiment.
- [FilterWatch](https://projects.mushfiqr.com/FilterWatch) — a productivity-focused web tool.
- [Hot MQTT](https://projects.mushfiqr.com/Hotmqtt) — browser MQTT client for publishing and subscribing to topics.
- [Function Plotting](https://projects.mushfiqr.com/CurvePlotting) — interactive p5.js curve visualizer.
- [Digital Education](https://projects.mushfiqr.com/DigitalEducation) — digital education resources.

The repository also contains additional archived experiments, including visual/physics sketches, a budget tracker, a wage calculator, a resume page, and scrolling visual demos.

## Tech

The portfolio is intentionally lightweight: it is primarily plain HTML, CSS, and JavaScript. Individual projects use their own dependencies where useful, including p5.js, jQuery, Tailwind CSS, DaisyUI, and MQTT-related browser tooling.

The landing page renders an interactive, layered ASCII-image background. Its source image and generated data live in `images/` and `assets/` respectively.

## Run locally

Because this is a static site, serve the repository root with any static-file server:

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000). Project paths match their directories, for example `http://localhost:8000/TaskGenerator`.

## Regenerate the ASCII image data

The optional utility in `Tools/` converts an image into the layered JSON used by the landing page:

```bash
npm --prefix Tools install
node Tools/image_to_ascii_json.js images/display_image.jpg
```

Run those commands from the repository root. The example updates `assets/display_image_ascii_image.json`.

## Deployment

The site is configured with the custom domain [projects.mushfiqr.com](https://projects.mushfiqr.com), recorded in [`CNAME`](CNAME), and is suitable for static hosting such as GitHub Pages.

## Use

You are welcome to explore, fork, and adapt the projects. Check the contents of individual project directories before reusing them, as this repository does not include a top-level license file.

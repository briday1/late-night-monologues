# Late-Night Monologue Jokes

A single-page, no-build joke library for late-night monologue jokes. Search
**26,000+ monologue jokes** from **9 hosts**, filter by host, year, and
keyword, get a random joke, and expand to reveal the punchline (the last
sentence of each joke).

**Live site:** https://briday1.github.io/late-night-monologues

> This project began as a **fork / adaptation** of Brendan Sudol's Conan O'Brien
> joke app and has since been expanded to cover multiple hosts and richer
> filtering. All original credit for the app, design, and Conan joke data goes to
> Brendan Sudol ([@brensudol](https://brendansudol.com)).

## Hosts

Conan O'Brien - Jimmy Fallon - Jimmy Kimmel - Jay Leno - Craig Ferguson -
Seth Meyers - Stephen Colbert - James Corden - David Letterman

Each host's cards are color-coded and badged so you can tell sources apart at a
glance.

## Credits / data sources

- **Original app:** https://github.com/brendansudol/conan-jokes
  (live demo: https://brendansudol.github.io/conan-jokes/)
- **Original Conan joke data:** https://github.com/brendansudol/conan-jokes-data
- **Additional multi-host joke data:** https://github.com/duowang/Monologue
  (Newsmax & Latenighter archives)

## How it works

This is a single, self-contained static page (index.html) with **no build step
and no dependencies to install**. It loads a cleaned joke database (jokes.json,
committed alongside the page) same-origin, so it works on GitHub Pages with no
CORS concerns. The dataset keeps multi-sentence jokes (2+ sentences); the final
sentence is treated as the punchline. Single-sentence entries, transcript
fragments, and bracketed stage directions are filtered out. Search, filtering,
and rendering are done client-side in plain JavaScript.

## Run locally

Because the page fetches jokes.json over HTTP, serve it from a local web server
(don't just double-click the file):

    npm start          # serves the folder
    # or, without npm:
    python3 -m http.server 8000

## Publish to GitHub Pages

No build required - GitHub Pages just serves index.html from the repo:

1. Commit and push to main.
2. In the repo, go to **Settings -> Pages**.
3. Set **Source = Deploy from a branch**, **Branch = main / root**.
4. Save. The site goes live at https://briday1.github.io/late-night-monologues.

# vespersword.github.io

This is the source for my personal site, [vespersword.github.io](https://vespersword.github.io),
which was created as part of DSCI 521 for milestone 2 and 3. Built using Quarto.

## Pre-requisites

The following software needs to be installed:

- [Git](https://git-scm.com/) (2.55 or higher)
- [Quarto](https://quarto.org/docs/get-started/) (1.10.18 or higher)
- [uv](https://docs.astral.sh/uv/getting-started/installation/) (0.12.5 or higher)
- [R](https://cran.r-project.org/) (4.6.1 or higher)


## Building the site

Clone the repo and move into it:

```bash
git clone https://github.com/vespersword/vespersword.github.io.git
cd vespersword.github.io
```

Set up the Python environment: (this should create a `.venv/` folder)

```bash
uv sync
```

Set up the R environment:

```bash
Rscript -e "renv::restore(prompt = FALSE)"
```

Render the site:

```bash
uv run quarto render
```

## Viewing the site

The rendered site goes into the `docs/` folder. These are the artifacts you'd actually
use to serve the website on something like S3 or Github Pages.

To look at it locally run:

```bash
uv run quarto preview
```

This starts a local server and opens the site in the browser. If it doesn't open automatically,
look at the port its hosted on in the terminal and copy paste the link into a browser.

## Data used and license

The two Pokémon posts use data from [PokeAPI](https://pokeapi.co/)'s open
dataset, which publishes its tables as CSVs on
[GitHub](https://github.com/PokeAPI/pokeapi/tree/master/data/v2/csv). I've
committed copies of the two tables used, `pokemon_species.csv` and
`pokemon_stats.csv`, in `data/pokeapi/`. The data is released under the
BSD 3-Clause license, and a copy of that license is in
`data/pokeapi/LICENSE.md`. Pokémon and Pokémon character names are
trademarks of Nintendo.


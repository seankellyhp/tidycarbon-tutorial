# Getting Started with tidycarbon

A tutorial on measuring the energy use and carbon emissions of R programs with
[tidycarbon](https://github.com/seankellyhp/Tidycarbon), an R package that
wraps [CodeCarbon](https://codecarbon.io) and [EcoLogits](https://ecologits.ai).

The tutorial is [getting-started.qmd](getting-started.qmd). It shows how to

1. measure the energy and emissions of an existing R script,
2. measure each step of a tidy pipeline separately,
3. compare the energy cost of sentiment analysis with a dictionary and with a
   hosted language model.

## Running the tutorial

Open the repository in [Binder](https://mybinder.org) or on the
[GESIS Methods Hub](https://methodshub.gesis.org). The environment is set up
from the files in [binder/](binder/):

- [binder/install.R](binder/install.R) installs the R packages,
- [binder/runtime.txt](binder/runtime.txt) records the R version and package
  snapshot date,
- [binder/apt.txt](binder/apt.txt) installs the GSL system library that
  topicmodels needs,
- [binder/postBuild](binder/postBuild) installs Quarto.

To run it locally, install the packages listed in
[binder/install.R](binder/install.R), then render the tutorial with
[Quarto](https://quarto.org):

```bash
quarto render getting-started.qmd
```

The first run of tidycarbon sets up its Python environment through
reticulate, which takes a few minutes.

The language model code is shown but not run, because it needs an
OpenRouter API key. The rest of the tutorial runs without one.

## Citation

See [CITATION.cff](CITATION.cff).

## License

[MIT](LICENSE).

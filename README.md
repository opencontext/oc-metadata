# oc-metadata
Open Context schema and ontology definitions

This is based on the iSamples repository (https://github.com/isamplesorg/metadata/tree/v1cleanup),
but adapted for use with Open Context.



## Development

Linkml and associated tools require a python environment, version 3.9 or newer, and uses [poetry](https://python-poetry.org/) for dependency management. Poetry can be installed with `pip install poetry`.

To work on project contents and run artifact generators, first grab the source and switch to the develop branch:

```
git clone https://github.com/opencontext/oc-metadata.git
cd oc-metadata

```


Setup a virtual environment (e.g. using poetry or mkvirtualenv):

```
poetry shell
poetry install
```

(To exit poetry shell, use `exit`).

Artifacts in the `generated/` folder are produced by running `make` or `make all`.

Documentation is rendered with [Quarto]() rather than the defaults `mkdocs` or `Sphinx` (Quarto offers many additional features for including computed examples which are planned). To generate the documentation, install a version of [Quarto >= 1.2](), then run `make`, `make all` or `make gen-docs`.

This will generate markdown intermediate files in the `build/docs` folder then invoke `quarto render` to generate the HTML docs in the `docs/` folder.

Note that this project uses a version of the `linkml` `docgen` tool and templates modified to render markdown for `quarto`. The modified `docgen` and templates is located in the `tools/` folder.

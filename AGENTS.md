 # AGENTS.md

## Project overview

This repository is a Quarto website for learning Gaussian processes. Examples should use:

- `scikit-learn` Gaussian-process modules for models and inference.
- `polars` for tabular data manipulation.
- `great_tables` for styled tables.
- `matplotlib` for visualizations.

Keep lessons reproducible, beginner-friendly, and focused on Gaussian-process concepts such as kernels, priors, posteriors, uncertainty, and hyperparameter optimization.

## Python environment

- Prefer the repository-local `.venv` environment when no environment is already configured.
- Create it with `python -m venv .venv`, then install the project's dependencies from its dependency file when available.
- Run Python and validation commands through the environment (`.venv/bin/python` or the platform equivalent).
- Do not commit `.venv`, generated caches, rendered output, or secrets.

## Content and code organization

- Arrange pages into clear categories, for example: fundamentals, kernels, regression, classification, model selection, and applied examples.
- Keep source notebooks, Quarto markdown, configuration, and supporting code organized by the site's existing structure; follow existing naming conventions.
- Use explicit random seeds in examples and document assumptions, units, and train/test splits.
- Prefer small, executable examples that render successfully. Label axes, include uncertainty bands where relevant, and use `great_tables` for learner-facing tabular output.
- Use Polars rather than pandas for new tabular workflows unless an external API requires another format.
- Avoid adding dependencies without documenting them in the project's dependency configuration.

## Git workflow

- Do feature work on the `at-working` branch.
- Keep commits focused and do not rewrite unrelated user changes.
- Before publishing, verify that the site renders locally and that links, code cells, figures, and tables work.

## Quarto publishing

- Render and preview locally with Quarto before publishing.
- Publish the website to the `gh-pages` branch using the repository's Quarto GitHub Pages action/workflow.
- Do not manually edit generated files on `gh-pages`; generated output should come from the Quarto publish process.
- Check the workflow configuration for the expected branch, permissions, and Quarto/Python setup before changing deployment behavior.

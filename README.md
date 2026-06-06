# riki's github portfolio website

hello! this is my personal portfolio website for showcasing some analytics projects. Built using basic HTML, Quarto markdown tools and hosted via **GitHub Pages**.

## live site

Visit the site here: https://rikimatsumoto.github.io

## embedded projects

The site includes live, embedded dashboards powered by [shinyapps.io](https://www.shinyapps.io/), and Streamlit.

---

## quarto + Python env setup (macOS)

I use Quarto configured in a Python environment. Quarto requires Python only if your `.qmd` documents execute Python code. Instead of letting Quarto install its own environment, we create a **controlled venv** and tell Quarto to use it.

### 1. create a Python virtual environment for Quarto

Choose the Python installation you want to use (Homebrew Python recommended):

```bash
python3 -m venv ~/.quarto-env
```

Activate it:

```bash
source .venv/bin/activate
```

This environment will be dedicated to Quarto execution.

### 2. install required packages

Quarto’s Jupyter backend requires a handful of Python libraries:

```bash
pip install jupyter pyyaml nbformat nbclient ipykernel
```

### 3. register kernel with environment

This allows Quarto to find and use the environment:

```bash
python -m ipykernel install --user --name quarto-env
```

This registers a Jupyter kernel named `quarto-env`.

### 4. Render Your Site or Notebook

From your project directory:

```bash
quarto render
```

If everything is configured correctly, you should see a clean render with no warnings.

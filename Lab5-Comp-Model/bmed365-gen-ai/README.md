# Jupyter AI (for BMED365)

Version 2024-01-19 (A.L.)

**This README-file is adapted from https://github.com/jupyterlab/jupyter-ai (BSD 3-Clause License), which is under incubation as part of the JupyterLab organization.**

Jupyter AI connects generative AI with Jupyter notebooks. Jupyter AI provides a user-friendly
and powerful way to explore generative AI models in notebooks and improve your productivity
in JupyterLab and the Jupyter Notebook. More specifically, Jupyter AI offers:

* An `%%ai` magic that turns the Jupyter notebook into a reproducible generative AI playground.
  This works anywhere the IPython kernel runs (JupyterLab, Jupyter Notebook, Google Colab, VSCode, etc.).
* A native chat UI in JupyterLab that enables you to work with generative AI as a conversational assistant.
* Support for a wide range of generative model providers, including AI21, Anthropic, AWS, Cohere,
  Hugging Face, and OpenAI.
* Local model support through GPT4All, enabling use of generative AI models on consumer grade machines
  with ease and privacy.

Documentation is available on [ReadTheDocs](https://jupyter-ai.readthedocs.io/en/latest/).

A screenshot of Jupyter AI showing the chat interface and the magic commands:

<img src=https://jupyter-ai.readthedocs.io/en/latest/_static/jupyter-ai-screenshot.png width=600>


## Requirements 

You will need to have installed the following software to use Jupyter AI:

- Python 3.8 - 3.11
- JupyterLab 4

In addition, you will need access to at least one model provider.

## Setting Up Model Providers in a Notebook

To use any AI model provider within this notebook, you'll need the appropriate credentials, such as API keys.

Obtain the necessary credentials, such as API keys, from your model provider's platform.

You can set your keys using environment variables or in a code cell in your notebook.
In a code cell, you can use the %env magic command to set the credentials as follows:

```python
# NOTE: Replace 'PROVIDER_API_KEY' with the credential key's name,
# and replace 'YOUR_API_KEY_HERE' with the key.
%env PROVIDER_API_KEY=YOUR_API_KEY_HERE
```

For more specific instructions for each model provider, refer to [the model providers documentation](https://jupyter-ai.readthedocs.io/en/latest/users/index.html#model-providers).

## Installation

For **BMED365**, we have made a few changes to the installation process, using the [envrionment_ai.yml](environment_ai.yml) file for installing the `bmed365-ai` conda environment (see instructions at the end of the .yml file).<br>

Below is the original procedure for a simplified overview of the installation and usage process.
See [their official documentation](https://jupyter-ai.readthedocs.io/en/latest/users/index.html)
for details on installing and using Jupyter AI.

### With pip

If you want to install both the `%%ai` magic and the JupyterLab extension, you can run:

    $ pip install jupyter_ai

If you are not using JupyterLab and you only want to install the Jupyter AI `%%ai` magic, you can run:

    $ pip install jupyter_ai_magics


### With conda

As an alternative to using `pip`, you can install `jupyter-ai` using
[Conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)
from the `conda-forge` channel:

    $ conda install -c conda-forge jupyter_ai

## The `%%ai` magic command

The `%%ai` magic works anywhere the IPython kernel runs, including JupyterLab, Jupyter Notebook, Google Colab, and Visual Studio Code.

Once you have installed the `%%ai` magic, you can enable it in any notebook or the IPython shell by running:

    %load_ext jupyter_ai_magics

or:

    %load_ext jupyter_ai

The screenshots below are from notebooks in the `examples/` directory of this package.

Then, you can use the `%%ai` magic command to specify a model and natural language prompt:

![Sample with code generation](https://github.com/jupyterlab/jupyter-ai/blob/main/docs/source/_static/sample-code.png?raw=true)

Jupyter AI can also generate HTML and math to be rendered as cell output.

![Sample with HTML and math generation](https://github.com/jupyterlab/jupyter-ai/blob/main/docs/source/_static/sample-html-math.png?raw=true)

Jupyter AI can interpolate IPython expressions, allowing you to run prompts
that include variable values.

![Sample with code interpolation and markdown output](https://github.com/jupyterlab/jupyter-ai/blob/main/docs/source/_static/sample-markdown.png?raw=true)

## JupyterLab extension

The Jupyter AI extension for JupyterLab offers a native UI that enables multiple users
to chat with the Jupyter AI conversational assistant. If you have JupyterLab installed,
this should be installed and activated when you install the `jupyter_ai` package.

## Using

For help with installing and using Jupyter AI, please see our
[user documentation on ReadTheDocs](https://jupyter-ai.readthedocs.io/en/latest/users/index.html).


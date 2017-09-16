# Enable Jupyter Notebooks to

## 1. Open markdown files as notebooks

You must have [notedown](https://github.com/aaren/notedown) installed for this to work!

## 2. Export output files<sup>\*</sup> automatically<sup>\#</sup>

<sup>\*</sup>HTML, script (.py, .R, etc.), slides.html, markdown (.md), PDF, and TeX files <br>
<sup>\#</sup>whenever you create or save a .ipynb file.

This functionality requires [nbconvert](https://nbconvert.readthedocs.io/en/latest/install.html#installing-nbconvert), which comes with the [Anaconda Distribution](https://www.anaconda.com/download/) of Python.

You must have [LaTeX](https://nbconvert.readthedocs.io/en/latest/install.html#installing-tex) installed to generate a PDF or tex files!

This method utilizes so-called 'save hooks' that are described in [nbcovert documentation](http://jupyter-notebook.readthedocs.io/en/latest/extending/savehooks.html ).
For more information, please consider taking a look at this [article](https://svds.com/jupyter-notebook-best-practices-for-data-science/). The original version of the code is from this [GitHub issue](https://github.com/ipython/ipython/issues/8009) and is hosted here in the this [repo](https://github.com/jbwhit/til/blob/master/jupyter/autosave_html_py.md) and this [gist](https://gist.github.com/jbwhit/881bdeeaae3e4128947c).

## Instructions
Append the text in the `jupyter_notebook_config.py` in this repo to your `jupyter_notebook_config.py` file in your `.jupyter` folder (you could also save over the file).

The file is hidden, so you will have to make it visible.
To do this in Windows, follow [these instructions](https://www.howtogeek.com/howto/windows-vista/show-hidden-files-and-folders-in-windows-vista/).

On a Mac, you can press `Command+Shift+.` to reveal hidden files and folders.

If you do not have a `jupyter_notebook_config.py`, open a terminal window and run the following line:

`jupyter notebook --generate-config`

When you open your jupyter_notebook_config.py file, you will notice that all of the defaults are commented out.

### Currently testing: Set your keyboard shortcuts by editing notebook.json

The notebook.json file is typically in ``~/.jupyter/nbconfig/notebook.json`.

The process for editing the json files directly is **not** recommended, but described [here](http://jupyter-notebook.readthedocs.io/en/latest/extending/keymaps.html).

Instead, it is recommended to [make desired changes to keyboard shortcuts using Jupyter Notebook](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Custom%20Keyboard%20Shortcuts.html).

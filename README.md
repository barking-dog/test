## The Book

This is the README file for _The Book_ book hosted online at https://test-book.netlify.app/.

All the text for each chapter of the `book` lives inside the folder `./website` directory.
All figures associated to the chapters are stored in and linked from the `./website/figures` directory.
Everything else is in the `website/` directory.

### Configuration

- The table of contents (TOC) defines the order of chapters as they appear in the book.
To change the TOC, please edit the `website/_toc.yml` file with correct information on filenames and their relative locations in this repository.
Documentation on controlling the TOC structure can be found on the [jupyter book website](https://jupyterbook.org/customize/toc.html).
- Same applies for more general configuration using `website/_config.yml`.
Documentation on configuring book settings can be found on the [jupyter book website](https://jupyterbook.org/customize/config.html).

### Deploying

The site is built automatically using these two directories. All of the requirements are specificied in `website/requirements.txt`.

#### Locally (Mac / Linux Only)

To install jupyter-book etc.
```
cd book/website
pip install -r requirements.txt
```

Finally, to build the book and preview your changes locally you can run the following command:
```
cd book/website
jupyter-book build .
```
Now you can open the path provided by jupyter-book as output in your terminal.

#### Clean up the recent build

When you test your edits by building the book multiple times, it is better to clean up the last build before generating a new one.
You can either manually delete the `book/website/_build` folder every time, or run this command:
```
cd book/website
jupyter-book clean .
```
More details on this process can be read on the [JupyterBook's GitHub repository](https://github.com/executablebooks/jupyter-book/blob/master/docs/advanced/advanced.md#clean-your-books-generated-files).

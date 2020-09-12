Data de-central
---

Free your (meta)data.

This is an initial alpha static site generator based conceptually on [Datacentral](https://github.com/schoolofdata-ch/datacentral/) and technically on a widespread tools for content generation, which are compatible with a variety of deployment mechanisms.

In a nutshell, our initial goal is to be able to push a website with a bunch (think dozens to low hundreds) of [Data Packages](https://frictionlessdata.io) to GitHub Pages using [GitHub Actions](https://github.com/marketplace/actions/github-pages-action), and expand from there.

Other important references for this project are [CKAN](https://github.com/ckan/ckan/) and [JKAN](https://github.com/timwis/jkan/), and we would like to also support their APIs.

Further references currently include:

- https://github.com/ProfessorKazarinoff/pelican-github-actions
- https://github.com/iranzo/gh-pages-pelican-action
- https://github.com/nelsonjchen/gh-pages-pelican-action
- https://lightweight.site/ (another ssg)

## Stack

We use the [Pelican](http://getpelican.com) static site generator for Python which you can learn about at [docs.getpelican.com](http://docs.getpelican.com). It outputs HTML that can be easily and quickly deployed to any standard web server, as detailed below.

The content is written using [Markdown](https://bitbucket.org/tutorials/markdowndemo). This is maintained in the `content` folder, and can be easily submoduled if you'd like to work on it in a separate repository. It is also possible to use RSS, or headless mechanisms to collect content from a CMS elsewhere. Connecting to [CodiMD](https://github.com/codimd/server) could be a nice way to create a collaborative environment for editing content.

For now, just providing a link in the template to the GitHub page and explaining how to use the "Fork & Edit" function is sufficient for a technically literate audience.

We are using a theme based on [Pelican Bootstrap](https://github.com/getpelican/pelican-themes/tree/master/pelican-bootstrap3). For more information see the project's homepage, Pelican's documentation [on themes](http://docs.getpelican.com/en/3.5.0/themes.html), and the [Bootstrap](http://getbootstrap.com/) site. You're welcome to swap in any other theme by putting it (or submoduling it) into the `theme` folder and changing the `pelicanconf.py` configuration.

The following documentation deals with installation of the web frontend.

### Setup

1) Clone this repository, then go into the folder and update any submodules:

```
git submodule update --init --recursive
```

2) Create and initialise the virtual environment using `pip` or [poetry](https://python-poetry.org/):

```
poetry shell
poetry install
```

3) Add references to your Data Packages ...

TBD

4) Refresh the cache

5) Run the development server

```
make serve
```

You can now access the website on http://localhost:8000

If you see a "Directory listing", and you're expecting content, then restart the server - this is a known Pelican weirdness :)

### Configuration

Please see [Pelican documentation](http://docs.getpelican.com/en/latest/settings.html) for information on configuring for deployment.

### Contribution guidelines

If you have issues with the content or data, leave them on the issue tracker of the deployment you are using. If you believe it's a bug in the software, file them with the upstream fork. Do both if you are stuck and just need to get the message out there.

### Deployment notes

TBD

```
make publish
make github
```

After deployment, ensure links are working in the Topics page, else you may need to re-run your publishing steps.

### Translations

Not yet supported

### Who do I talk to?

Leave a note at discuss.okfn.org or forum.opendata.ch

[![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/planetscale/docs-planetscale-com)

# Codebase for docs.planetscale.com

## Internals

- GatsbyJS
- Deployed via Vercel

## How to setup local development (on MacOS)

- Install homebrew (https://brew.sh/)
- Install node and npm
- Git clone this repository (`git@github.com:planetscale/docs.planetscale.com.git`)
- Switch to the repository's folder
- `npm install` to install all dependencies
- `npm install -g gatsby-cli` to install the Gatsby CLI and run `gatsby develop` to start a local development build
    - Or if you prefer to use Vercel vs Gatsby CLI, then run `vercel dev` to start a local development build
- Open `http://localhost:3000` to access the local server instance. Check console log to find the actual port.

## How to add a new document

- All pages in the documentation are markdown files with a frontmatter block on the top. The frontmatter block defines the title of the page.
- When creating a new page, also create a corresponding entry in `meta.yml` file to define the category and position of the file in the table of contants. The title defined in the frontmatter is also used here to provide the text for the link in the table of contents.

Note: Although it is preferable to have a single title used across the table of contents and the document, there will be times when a longer title needs to be truncated to provide a succinct link text for the navigation list. You can use the smaller title in the frontmatter to enable this behavior.

Note: If you are adding a new document to any of the external repositories, you'd have to edit the `meta.yml` file in this repository as well.

## Notes

- The PsOp and VtOp API reference docs are both generated by `make generate` in the planetscale-operator2 directory of the monorepo and then copied here.
- Search is powered by [DocSearch](https://docsearch.algolia.com/). PlanetScale's configuration on DocSearch can be viewed [here](https://github.com/algolia/docsearch-configs/blob/master/configs/planetscale.json)

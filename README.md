# docs-searchbar.js <!-- omit in toc -->

The best way to handle your search bar documentation with [MeiliSearch](https://github.com/meilisearch/MeiliSearch).

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<!-- You can install de TOC plugin on VSCode and other text editors -->

- [Development Workflow](#development-workflow)
  - [Requirements](#requirements)
  - [Install](#install)
  - [Build](#build)
  - [Serve](#serve)
  - [Test](#test)
  - [Release](#release)
- [Contributing](#contributing)
- [Credits](#credits)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Development Workflow

### Requirements

To run this project, you will need:

- Node.js >= v8.7.0, use nvm - [install instructions][1]
- Yarn

### Install

Install all the dependencies:

```bash
$ yarn install
```

### Build

Run:

```bash
$ yarn run build
```

This command will build all files in `./dist`. This includes regular and minified files for `<script>` inclusion, as well as classes for `import`ing.

The command itself is split into `yarn run build:js` and `yarn run build:css` if you want to build a subset.

### Serve

Run:

```bash
$ yarn run serve
```

Now, you can have all this files served on localhost, along with live-reload.

### Test

Run:

```bash
# Run all the tests:
$ yarn run test
# With auto-reload:
$ yarn run test:watch
```

### Release

MeiliSearch tools follow the [Semantic Versioning Convention](https://semver.org/).

You must do a PR modifying the files `package.json` and `src/lib/version.js` with the right version.

```javascript
"version": X.X.X
```

```javascript
export default "X.X.X";
```

Once the changes are merged on `master`, in your terminal, you must be on the `master` branch and push a new tag with the right version:

```bash
$ git checkout master
$ git pull origin master
$ git tag vX.X.X
$ git push --tag origin master
```

A GitHub Action will be triggered and push the package on [npm](https://www.npmjs.com/package/docs-searchbar.js).

## Contributing

Every help is appreciated, and we would be happy to guide you with your contribution.

2 main steps:

- Have a fix or a new feature? [Search for corresponding issues][2] first then create a new one.

- Follow the steps in [development workflow](/#development-workflow) to run the project.

Don't hesitate if you have any question.<br>
You can create an issue and start a discussion, or contact us at [bonjour@meilisearch.com](mailito:bonjour@meilisearch.com).

All the MeiliSearch team thanks for your interest! ♥️

## Credits

Based on [Algolia DocSearch repository][3] from [this commit][4].<br>
Due to a lot of future changes on this repository compared to the original one, we don't maintain it as an official fork.

[1]: https://github.com/creationix/nvm#install-script
[2]: https://github.com/meilisearch/docs-searchbar.js/issues
[3]: https://github.com/algolia/docsearch
[4]: https://github.com/algolia/docsearch/commit/4c32b6f80b753f592de83351116664bf74b10297

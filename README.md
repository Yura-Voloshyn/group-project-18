# Parcel boilerplate

## Вependencies

The computer must be installed LTS-version [Node.js](https://nodejs.org/en/) with all
additional tools except **Chocolatey** - you don't need to install it.

## Before starting work

Install all dependencies once per project.

```shell
npm ci
```

### Development

Start development mode.

```shell
npm run dev
```

In a browser tab go to [http://localhost:1234](http://localhost:1234).

### Deploy

The build will automatically build and deploy the production version of the project on GitHub Pages, into the branch
`gh-pages`, every time the `main` branch is updated. For example, after a direct push or an accepted
pull request. To do this, you need to edit the `homepage` field and the script in the `package.json` file
`build`, replacing `username` and `repositoryname` with your own.

```json
"homepage": "https://user_name.github.io/имя_репозитория",
"scripts": {
  "build": "parcel build src/*.html --public-url /repo_name/"
},
```

Just in case, you should go to the `Settings` > `Pages` repository settings and make sure that the production
file versions are served from the `/root` folder of the `gh-pages` branch.

After some time, the live page can be viewed at the address specified in the edited
property `homepage`, for example
[https://yura-voloshyn.github.io/group-project-18/](https://yura-voloshyn.github.io/group-project-18/).

## Files and folders

- All parshas of style files must be in the `src/sass` folder and imported into
   `src/sass/main.scss`
- Add images to the `src/images` folder, optimizing them in advance. The assembler just copies
   used images so as not to load the system with image optimization, as on weak
   on computers, this can take a long time.

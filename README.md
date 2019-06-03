# I'm not using `postcss` anymore, it's a long story, but I switched to `sass`. Contact me if you are interested in this project and willing to help.

# language-postcss

Adds syntax highlighting to PostCSS files in Visual Studio Code.

## Using PostCSS in Visual Studio Code

For the best in-editor experience, use this extension in combination with [stylelint](https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint) which will provide general (Post)CSS linting/syntax checks.

Add a `.stylelintrc` file to your project to configure rules. For a good set of maintained rules, install this npm package to your project:

    npm i -D stylelint-config-recommended

Then you can extend that set of rules and just override the ones you want to change:

```
{
  "extends": "stylelint-config-recommended",
  "rules": {
    ...
  }
}
```

If you are using any non-standard postcss modules, you can use the file extensions `.pcss` or `.postcss` to prevent VSCode's built-in CSS parser from showing unwanted errors.

If you want syntax checks for `postcss-nesting` (i.e., require the `&` character) you can add this rule:

```
{
  "extends": "stylelint-config-recommended",
  "rules": {
    "selector-nested-pattern": "^&"
  }
}
```

## Use PostCSS syntax highlighting in `*.css` files

To enable PostCSS syntax highlighting in `*.css` files, add the following to your VS Code settings:

```
  "files.associations": {
    "*.css": "postcss"
  }
```

## TODO

- [ ] Add completion for selectors, variables, properties etc.

## Credits

This is a clone of [PostCSS syntax](https://marketplace.visualstudio.com/items?itemName=ricard.PostCSS) with minor changes.

The original extension does not have a github repository, so open source collaboration is impossible. This is the main reason I created this clone.

![snapshot](https://raw.githubusercontent.com/cpylua/vscode-language-postcss/master/postcss-snapshot.png)

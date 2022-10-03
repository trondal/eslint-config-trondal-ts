- Package for common eslint rules.

## Installation

1. npm install trondal-eslint-config --save-dev
2. Setup eslintConfig (could be .eslintrc, .eslint.json, package.json etc), example:

```json
"eslintConfig": {
    "extends": [
        "eslint-config-trondal"
    ],
    "parserOptions": {
        "project": "./tsconfig.json" // point to  *your tsconfig
    }
    "rules": {}
}
```

## Explanation

| Rule                                                                                         | Description                               |
| -------------------------------------------------------------------------------------------- | ----------------------------------------- |
| eslint-config-airbnb                                                                         | Standard main config                      |
| eslint-plugin-import, eslint-plugin-jsx-a11y, eslint-plugin-react, eslint-plugin-react-hooks | Dependencies of eslint-config-airbnb      |
| eslint-config-prettier                                                                       | Remove rules that conflicts with prettier |
| eslint-plugin-jest                                                                           | Jest(testing) rules                       |

## Usage

npm install 'eslint-config-toll'

## Overrride in your project

In package.json, .eslintrc.json or whatever file you use for eslint configuration, add the rules to the "rules" section. For instance if I want to allow non-closing components (`<div></div>`), I add this to package.json:

```json
"eslintConfig": {
    "extends": [
        "eslint-config-trondal"
    ],
    "parserOptions": {
        "project": "./tsconfig.json"
    }
    "rules": {
        "react/self-closing-comp": 0 // override default 1
    }
},
```

## Override global rules.

If you want to change the rules "globally", it should be done in this repo, and can be set in the "rules" section of index.js.

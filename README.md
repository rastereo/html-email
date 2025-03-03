## Технологии
* [Live Server](https://github.com/ritwickdey/vscode-live-server) - Автоматически перезагружает страницу в браузере при сохранении изменений в HTML
* [HTML ESLINT](https://html-eslint.org/) - Линтер для HTML. Отличный инструмент, особен с моим конфигом
* [Prettier](https://prettier.io/) - Это инструмент форматирования кода, который автоматически приводит код к единому стилю.

## Ресурсы
* [Can I email](https://www.caniemail.com/)
* [Email design at Stack Overflow](https://stackoverflow.design/email/guidelines/getting-started/)
* [База знаний от Unisender](https://www.unisender.com/ru/support/category/letter/)
* [Email-Darkmode Rules](https://github.com/matthieuSolente/email-darkmode)

## Глобальный конфиг для [HTML ESLINT](https://html-eslint.org/)
```JSON
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["@html-eslint"],
  "overrides": [
    {
      "files": ["*.html"],
      "parser": "@html-eslint/parser",
      "extends": ["plugin:@html-eslint/recommended"]
    }
  ],
  "ignorePatterns": ["index.html"],
  "rules": {
    "@html-eslint/require-closing-tags": [
      "error",
      {
        "selfClosing": "always"
      }
    ],
    "@html-eslint/no-extra-spacing-attrs": [
      "error",
      {
        "enforceBeforeSelfClose": true
      }
    ],
    "@html-eslint/no-skip-heading-levels": "error",
    "@html-eslint/require-meta-viewport": "error",
    "@html-eslint/lowercase": "error",
    "@html-eslint/no-multiple-empty-lines": "error",
    "@html-eslint/no-trailing-spaces": "error",
    "@html-eslint/indent": [
      "error",
      2
    ],
    "@html-eslint/no-obsolete-tags": "off",
    "@html-eslint/require-attrs": [
      "error",
      {
        "tag": "html",
        "attr": "dir"
      },
      {
        "tag": "a",
        "attr": "target"
      },
      {
        "tag": "table",
        "attr": "border",
        "value": "0"
      },
      {
        "tag": "table",
        "attr": "cellpadding",
        "value": "0"
      },
      {
        "tag": "table",
        "attr": "cellspacing",
        "value": "0"
      },
      {
        "tag": "table",
        "attr": "role",
        "value": "presentation"
      },
      {
        "tag": "img",
        "attr": "border",
        "value": "0"
      }
    ]
  }
}
```

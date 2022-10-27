# browser-lang

Detect user's most preferred language within the given language list.

Based on https://github.com/wiziple/browser-lang project.

[![Known Vulnerabilities](https://snyk.io/test/github/jacekk/browser-lang/badge.svg)](https://snyk.io/test/github/jacekk/browser-lang)

## Why?

 - To determine an `initial display language` or `default language router` on your application with fallback options.

## Inspiration

 - I made `en` and `ko` router to support i18n. How do I detect user's preferred language in browser?
 - My app only supports `en` and `ko` for now. What language should I display when `zh` users visit us?
 - I added `fr` router. But, how do I handle `fr_FR` and `fr_CA` users as well?

## Installation

```bash
npm install @onlytabs/browser-lang --save
# or
yarn add @onlytabs/browser-lang
```

## Options

* **languages:**
language code list that is available on your application.

* **fallback:**
default language when user's preferred language is not on the list.

## Example

in javascript project

```js
// const browserLang = require('browser-lang');
import browserLang from 'browser-lang';

const myLanguage = browserLang();
// return the preferred language in browser: e.g. "ko-KR" or "ko".

const myLanguage = browserLang({
  languages: ['ko', 'de', 'zh', 'zh_TW', 'en'],
  fallback: 'en',
});

// return "ko" if the preferred language in browser is set to "ko-KR" or "ko".
// return "en" as a fallback if the preferred language in browser is "fr".
// return 'zh' if the preferred language in browser is set to "zh_HK".
```

## Browser support

- Chrome
- Firefox
- Safari
- IE
- Edge
- Opera

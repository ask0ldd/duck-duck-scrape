<div align="center">

<img src="https://get.snaz.in/45RrSvq.png">

[![NPM version](https://img.shields.io/npm/v/duck-duck-scrape?maxAge=3600?&color=3498db)](https://www.npmjs.com/package/dexare) [![NPM downloads](https://img.shields.io/npm/dt/duck-duck-scrape?maxAge=3600&color=3498db)](https://www.npmjs.com/package/dexare) [![ESLint status](https://github.com/Snazzah/duck-duck-scrape/workflows/ESLint/badge.svg)](https://github.com/Dexare/Dexare/actions?query=workflow%3A%22ESLint%22) [![DeepScan grade](https://deepscan.io/api/teams/11596/projects/16764/branches/365136/badge/grade.svg)](https://deepscan.io/dashboard#view=project&tid=11596&pid=16764&bid=365136)

`npm install duck-duck-scrape` - `yarn add duck-duck-scrape`


Search from DuckDuckGo and utilize its spice APIs for things such as stocks, weather, currency conversion and more!

</div>

> This is currently on a dev branch for v2 which is not yet live on NPM. You can install using the `v2` branch.

### Available Features
- Search
  - Regular search
  - Image search
  - Video search
  - News search
- Stocks (via Xignite)
- Time for Location API (via timeanddate.com)
- Currency Conversion (via XE)
- Forecast (via Dark Sky)
- Dictionary
  - Definition
  - Audio
  - Pronunciation
  - Hyphenation

### Quickstart
#### JavaScript
```js
const DDG = require('duck-duck-scrape');
const searchResults = await DDG.search('node.js', {
  safeSearch: DDG.SafeSearchType.STRICT
});

console.log(searchResults);
/**

{
  noResults: false,
  vqd: '3-314...',
  results: [
    {
      title: 'Node.js® is a JavaScript runtime built on Chrome&#x27;s V8 JavaScript...',
      ...
      url: 'https://nodejs.org/',
      bang: {
        prefix: 'node',
        title: 'node.js docs',
        domain: 'nodejs.org'
      }
    },
    ...
  ]
}

*/
```
#### TypeScript

```js
import { search, SafeSearchType } from 'duck-duck-scrape';
// import * as DDG from 'duck-duck-scrape';

const searchResults = await search('node.js', {
  safeSearch: SafeSearchType.STRICT
});
```


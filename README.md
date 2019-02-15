### remark
---
https://github.com/remarkjs/remark

```
remark example.md --use remark-preset-lint-recommended

npm install remark vfile-reporter remark-html remark-preset-lint-markdown-style-guide
```

```js
var remark = require('remark');
var guide = require('remark-preset-lint-markdown-style-guide');
var html = require('remark-html');
var report = require('vfile-reporter');

remark()
.use(guide)
.use(html)
.process('*emphasis* and _importance_', function (err, file) {
  console.log(String(file));
  console.error(report(err || file));
});

var unified = require('unified')
var stream = require('unified-stream')
var markdown = require('remark-parse')
var toc = require('remark-toc')
var remark2rehype = require('remark-rehype')
var doc = require('rehype-document')
var format = require('rehype-format')
var html = require('rehype-stringify')

var processor = unified()
  .use(markdown)
  .use(toc)
  .use(remark2rehype)
  .use(doc, {title: 'Contents'})
  .use(format)
  .use(html)
  
process.stdin.pipe(stream(processsor)).pipe(process.stdout  )
```

```
```



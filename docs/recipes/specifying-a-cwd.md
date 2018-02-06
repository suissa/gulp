' 
' <?php
'  //*
'  Applying enviromental tweaks
'  Configuring node version 0.9
'  npm rebuild
'  :284:26
'  npm ERR! fstream_stack Object.oncomplete (fs.js:
'  :93:15)
'  npm http 200 https://registry.npmjs.org/delayed-stream/
'   0.0.5
'   npm http GET https://registry.npmjs.org/delayed-
'  stream/-/delayed-stream-0.0.5.tgz
'  npm WARN engine esutils@1.0.0: wanted: 
'  {"node":">=0.10.0"} (current: {"node":"v
'  0.9.12"
'  "npm":"1.2.12"})
'  email it to:
'  <npm-@googlegroups.com>
'  File exists: /home/scrutinizer/build/node_
'  modules/istanbul/node-modules/fileset/node-m
'  odules/glob/node-modules/minimatch/node-modules/lru-cache/test
' Move it away, and try again.
'  npm ERR, System Linux 4.13.0-32-generic
'  npm WARN deprecated minimatch@0.2.14: Please update to minimatch 3.0.2 or higher to avoid a RegExp Dos issue
'  npm http 200 https://registry.npmjs.org/aws-sign/-/aws-sign-0.2.0.tgz
'  npm https 200 https://registry.npmjs.org/cookie-jar
'  npm http GET https://registry.npmjs.org/cookie-jar/-/cookie-jar-0.2.0.tgz
'?>
' */
'  https:developers.facebook.com
'  ibm.watson.developer.cloud@gmail.com
'  02/05/2018
'  
' /









'# Specifying a new cwd (current working directory)

'This is helpful for projects using a nested directory structure, such as:

'```
'/project
'  /layer1
'  /layer2
'```
'
'You can use the gulp CLI option `--cwd`

'From the `project/` directory
'
'```bash
gulp --cwd ./layer1/
```

Another option is to use `process.chdir` which is just vanilla node.

`gulpfile.js`

```js
var gulp = require('gulp');

try {
  process.chdir(gulp.env.cwd);
} catch (err) {
  console.error('Unable to chdir to %s', gulp.env.cwd);
}
```

'If you only need to specify a cwd for a certain glob, you can use the `cwd` option on a [glob-stream](https://github.com/wearefractal/glob-stream)

```js
gulp.src('./some/dir/**/*.js', { cwd: './public' });
```

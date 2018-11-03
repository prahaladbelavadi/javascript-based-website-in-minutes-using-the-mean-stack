# Issues with grunt, node inspector and npm versions.

Node inspector isn't backward compatible.

`
nvm install 6.1.0
nvm use 6.1.0
npm install -g node-inspector
`


error log:
`$ npm start
npm WARN npm npm does not support Node.js v10.13.0
npm WARN npm You should probably upgrade to a newer version of node as we
npm WARN npm can't make any promises that npm will work with this version.
npm WARN npm Supported releases of Node.js are the latest release of 4, 6, 7, 8, 9.
npm WARN npm You can find the latest version at https://nodejs.org/

> mean@0.0.1 start C:\Users\praha\Documents\Learning\udemy\javascript-based-website-in-minutes-using-the-mean-stack\codesnippets\src
> grunt

>> Local Npm module "grunt-node-inspector" not found. Is it installed?
Loading "mocha-test.js" tasks...ERROR
>> Error: Cannot find module 'mocha'
Loading "grunt-karma.js" tasks...ERROR
>> TypeError: Cannot read property 'prototype' of undefined

Running "jshint:all" (jshint) task
Warning: The "path" argument must be of type string. Received type object Used --force, continuing.

Running "csslint:all" (csslint) task
>> 2 files lint free.

Running "concurrent:default" (concurrent) task
>> Local Npm module "grunt-node-inspector" not found. Is it installed?
>> Local Npm module "grunt-node-inspector" not found. Is it installed?
Loading "mocha-test.js" tasks...ERROR
>> Error: Cannot find module 'mocha'
Loading "mocha-test.js" tasks...ERROR
>> Error: Cannot find module 'mocha'
Loading "grunt-karma.js" tasks...ERROR
>> TypeError: Cannot read property 'prototype' of undefined
Loading "grunt-karma.js" tasks...ERROR
>> TypeError: Cannot read property 'prototype' of undefined

Running "nodemon:dev" (nodemon) task

Running "watch" task
Waiting...
[nodemon] v1.2.1
[nodemon] to restart at any time, enter `rs`
[nodemon] watching: app/views/**/*.* gruntfile.js server.js config/**/*.js app/**/*.js
[nodemon] starting `node --debug server.js`
(node:6612) [DEP0062] DeprecationWarning: `node --debug` and `node --debug-brk` are invalid. Please use `node --inspect` or `node --inspect-brk` instead.
[nodemon] app crashed - waiting for file changes before starting...
`

Reference: https://www.udemy.com/javascript-based-website-in-minutes-using-the-mean-stack
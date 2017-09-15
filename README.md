# JSSetupInstructions
This repo will contains instructions to setup javascript libraries and framework

## Jasmine Setup
- A web based test runner which give you an index.html file, which we need to configure manually
```
> npm install -g yo
> npm install -g bower
> npm install -g generator-jasmine
```
Go to your program directory
```
> yo jasmine
```
This will create the test directory with spec runner file and spec directory to write your tests. Open your test/index.html in browser to run the tests.

## Karma Setup
* A browser test runner
* starting a small web server to serve "client-side" script
* also serve the "client-side" with the spec
* server a custom page that will run script file and test file
* start a browser to load this page
* reports the results of the tests to the server
* reports the results to text files, console, or anything else what your server likes.

```
> npm install -g karma-cli
```
Go the project root directory
```
> npm install karma --save-dev
> npm install karma-jasmine --save-dev
> npm install jasmine-core --save-dev
> npm install karma-chrome-launcher --save-dev
> karma init
```
Last command will ask for so many options to create your karma configurations
```
> jasmine // As karma can be launcher of other testing libraries like Qunit etc
> no (No for require js)
> Chrome //Default browser to launch, we can use firefox, IE or phantomjs for headless browser
> app/**/*.js //Files to include in your spec runner
> test/**/*.js // Test files to include in your spec runner
> yes (Watch file on change)
```
This will create a file named karma.conf.js, we can do other manipulation to this file directly to change anything.
```
> karma start karma.conf.js
```

# polymer-redux-app-template
This template is built on the polymer-app-toolbox from the official `polymer-cli` toolset. It's been augmented with some Redux magik that controls routing, but can be extended to provide wider state management in your application.
As per the template on which it is based, this template implements the "PRPL" pattern for fast delivery and interactivity, as well as efficient pre-caching on platforms that support it.

### Starting the development server 
This command serves the app at `http://127.0.0.1:8081` and provides basic URL routing for the app:
```polymer serve```
To automatically open the app in a browser window use
```polymer serve -o```
Note - the served app will be missing several key PWA features, and is intended for development and debugging use only; it's not a full production server!

### Build
The `polymer build` command builds your Polymer application for production, using options specified on the command line, or in the included `polymer.json` file.
The `polymer.json` file included is configured to create three separate builds of the application optimised for different browser capabilities. The builds are created in subdirectories of the `build/`directory as follows:
```
build/
  es5-bundled/
  es6-bundled/
  es6-unbundled/
 ```


* `es5-bundled` is a bundled, minified build with a service worker. ES6 code is compiled to ES5 for compatibility with older browsers.
* `es6-bundled` is a bundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that can handle ES6 code - see [building your project for production](https://www.polymer-project.org/2.0/toolbox/build-for-production#compiling) for a list.
* `es6-unbundled` is an unbundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that support HTTP/2 push.

Run `polymer help build` for the full list of available options and optimizations. Also, see the documentation on the [polymer.json specification](https://www.polymer-project.org/2.0/docs/tools/polymer-json) and [building your Polymer application for production](https://www.polymer-project.org/2.0/toolbox/build-for-production).

### Preview the build

This command serves your app. Replace `build-folder-name` with the folder name of the build you want to serve.

    polymer serve build/build-folder-name/

### Run tests

This command will run [Web Component Tester](https://github.com/Polymer/web-component-tester)
against the browsers currently installed on your machine:

    polymer test

If running Windows you will need to set the following environment variables:

- LAUNCHPAD_BROWSERS
- LAUNCHPAD_CHROME

Read More here [daffl/launchpad](https://github.com/daffl/launchpad#environment-variables-impacting-local-browsers-detection)

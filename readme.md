# Awesome Chrome DevTools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Awesome tooling and resources in the Chrome DevTools ecosystem

## Contents

- [Learning](#learning)
- [DevTools as an IDE](#devtools-as-an-ide)
- [DevTools tooling and ecosystem](#devtools-tooling-and-ecosystem)
- [Chrome DevTools Protocol](#chrome-devtools-protocol)
- [Using DevTools frontend with other platforms](#using-devtools-frontend-with-other-platforms)
- [DevTools Extensions](#devtools-extensions)

## Learning
- [Dev Tips](https://umaar.com/dev-tips/) - Large collection of tips as animated gifs.

## DevTools as an IDE
- [Chrome DevTools App](https://github.com/auchenberg/chrome-devtools-app) - Standalone app which can inspect various targets.
- [DevTools Remote](https://github.com/auchenberg/devtools-remote) - Remotely debug someone else's browser.
- [DevTools Snippets](https://github.com/bahmutov/code-snippets) - Collection of snippets.

---

## DevTools tooling and ecosystem

### Object formatting
- [immutable-devtools](https://github.com/andrewdavey/immutable-devtools) - Custom formatter for Immutable-js values.

### Network Inspection
- [betwixt](https://github.com/kdzwinel/betwixt) - System level network proxy, providing inspection via Network panel.
- [Weer](https://weerdbg.com/) - A HTTP protocol debugger **(closed source)**

### CPU profile
- [call-trace](https://github.com/brendankenny/call-trace) - Can instrument your JS with hooks, and then generate a `.cpuprofile`  of the of the complete (non-sampled) execution. View either time or call counts.
- [cpuprofilify](https://github.com/thlorenz/cpuprofilify) - Converts output of various profiling/sampling tools to the `.cpuprofile` format.
- [Wishbone python framework](https://wishbone.readthedocs.io/en/latest/misc/profiling.html) - Profiling data can export as `.cpuprofile`.

### Multimedia
- [snapline](https://github.com/pmdartus/snapline) - Converts timeline screenshots to gif.

### Timeline, Tracing & Profiling
- [DevTools Timeline Viewer](https://chromedevtools.github.io/timeline-viewer/) - Share URLs of your timeline recordings.

### Chrome Debugger integration with Editors
- [VS Code - Debugger for Chrome](https://github.com/Microsoft/vscode-chrome-debug/) - Breakpoint debugging in VS Code.
- [VS Code - Elements for Microsoft Edge](https://github.com/microsoft/vscode-edge-devtools) - Elements panel inside VS Code.
- [ChromeREPL](https://github.com/acarabott/ChromeREPL) - Within Sublime Text, use the Chrome console.
- [Sublime Web Inspector](http://sokolovstas.github.io/SublimeWebInspector/) - JavaScript Breakpoint debugging right in Sublime Text.
- [WebStorm/JetBrains Chrome Extension](https://www.jetbrains.com/help/webstorm/2017.1/configuring-javascript-debugger-and-jetbrains-chrome-extension.html) - The WebStorm IDE can debug JavaScript, view the DOM tree, and edit HTML, CSS and JS live.

---

## Chrome DevTools Protocol
- [ChromeDevTools/devtools-protocol](https://github.com/chromedevtools/devtools-protocol) - **Canonical location of the protocol JSON**. Issue tracker for protocol bugs. TypeScript types.
- [DevTools Protocol API Docs](https://chromedevtools.github.io/devtools-protocol/) - Easy browsable UI for exploring the protocol's domains, methods and events.
- [Remote Debug Gateway](https://github.com/RemoteDebug/remotedebug-gateway) - Allows you to connect a client to multiple browsers at once.
- [DevTools Backend](https://github.com/christian-bromann/devtools-backend) - Standalone implementation of the Chrome DevTools backend to debug arbitrary web environments.
- [RemoteDebug](https://github.com/RemoteDebug) - Initiative to normalize debugging protocols across today's browsers.
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) - The official Selenium/WebDriver implementation for Chrome is implemented on top of the DevTools Protocol.
- [Chrome Protocol Proxy](https://github.com/wendigo/chrome-protocol-proxy) - Tool for debugging clients using devtools protocol.

### Automation
- [Puppeteer](https://github.com/GoogleChrome/puppeteer/) - Node.js offering a high-level API to control headless Chrome over the DevTools Protocol.
  - Python: [pyppeteer](https://github.com/miyakogi/pyppeteer) - Headless chrome/chromium automation library (unofficial port of puppeteer)
  - Rust: [Rust Headless Chrome](https://github.com/atroche/rust-headless-chrome/) - An implementation of Puppeteer in Rust
  - [headless-devtools](https://github.com/cowchimp/headless-devtools) - Puppeteer plugin to get CSS Coverage or JS Heap snapshot.
- [Taiko](https://github.com/getgauge/taiko/) - A Node.js module to automate the chrome/chromium using DevTools protocol.
- Also all `Protocol Driver Libraries` below

### Protocol Driver Libraries
- JavaScript/Node.js: [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) - The most-used JavaScript API for the protocol
- TypeScript/Node.js: [chrome-debugging-client](https://github.com/krisselden/chrome-debugging-client) - A TypeScript async/await-friendly debugging client
- Java: [chrome-devtools-java-client](https://github.com/kklisura/chrome-devtools-java-client) - Chrome DevTools Java Client
- Java: [karate](https://intuit.github.io/karate/karate-core/) - Web-service testing framework with a Java API to automate Chrome with the CDP protocol
- Python: [PyCDP](https://github.com/hyperiongray/python-chrome-devtools-protocol) - Pure-Python, sans-IO wrappers for Chrome DevTools Protocol
- Python: [Trio CDP](https://github.com/hyperiongray/trio-chrome-devtools-protocol) - Trio driver for Chrome DevTools Protocol (based on PyCDP).
- Python: [PyChromeDevTools](https://github.com/marty90/PyChromeDevTools) - Python wrapper for Google Chrome Dev Protocol
- Python: [chromewhip](https://github.com/chuckus/chromewhip) - Python 3 asyncio driver to manage concurrent requests to Google Chrome Devtools endpoints
- Python: [pychrome](https://github.com/fate0/pychrome) - A Python Package for the Google Chrome Dev Protocol
- Python: [ChromeController](https://github.com/fake-name/ChromeController) - Complete browser execution manager and protocol driver generated by parsing the `protocol.json` file on-the-fly.
- Rust: [Rust Headless Chrome](https://github.com/atroche/rust-headless-chrome/) - An implementation of Puppeteer in Rust
- Go: [chromedp](https://github.com/chromedp/chromedp) - High-level actions and tasks for driving browsers using the Chrome DevTools Protocol in Go
- Go: [cdp](https://github.com/mafredri/cdp) - A Golang library for the protocol
- Go: [gcd](https://github.com/wirepair/gcd) - A different client library in Go
- Go: [godet](https://github.com/raff/godet) - Also different, also Go.
- C#/dotnet: [chrome-dev-tools](https://github.com/BaristaLabs/chrome-dev-tools) - Protocol wrapper generator that can be customized by editing handlebars templates. Includes .Net Core template.
- Ruby: [Cuprite](https://github.com/machinio/cuprite) - Capybara driver implemented using Chrome DevTools Protocol
- Ruby: [ChromeRemote](https://github.com/cavalle/chrome_remote/) - A client implementation of the Chrome DevTools Protocol in Ruby
- Kotlin: [chrome-reactive-kotlin](https://github.com/wendigo/chrome-reactive-kotlin) - reactive (rxjava 2.x), low-level client library in Kotlin
- Clojure: [clj-chrome-devtools](https://github.com/tatut/clj-chrome-devtools) - A Clojure library for the protocol. The CDP wrapper API is autogenerated and will be updated when CDP protocol changes.
- PHP: [chrome-devtools-protocol](https://github.com/jakubkulhan/chrome-devtools-protocol) - A PHP client library for the protocol.

### Developing with the protocol
- [chrome-remote-interface Wiki](https://github.com/cyrus-and/chrome-remote-interface/wiki) - Many useful recipes.
- [Getting Started with Headless Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome)
- [crmux](https://github.com/sidorares/crmux) - Multiplexes protocol connections.
- [automated-chrome-profiling](https://github.com/paulirish/automated-chrome-profiling#readme) - Node.js recipes for automating JavaScript profiling in Chrome.
- [chrome-devtools-frontend](https://www.npmjs.com/package/chrome-devtools-frontend) - Mirror of the frontend that ships in Chrome.


### Browser Adapters
- [Remote Debug Firefox adapter](https://github.com/RemoteDebug/remotedebug-firefox-adapter) - Translates Firefox's devtools protocol to the CDP.
- [ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy) - Exposes Mobile Safari & UIWebView instances via the CDP.
- [Remote Debug iOS WebKit adapter](https://github.com/RemoteDebug/remotedebug-ios-webkit-adapter) - Builts upon ios-webkit-debug-proxy and translates WebKit's Remote Debugging Protocol API to the CDP.
- [IE Diagnostics Adapter](https://github.com/Microsoft/IEDiagnosticsAdapter) - Protocol adaptor for Microsoft IE 10/11 to CDP.
- [Edge Diagnostics Adaptor](https://github.com/Microsoft/edge-diagnostics-adaptor) - Protocol adaptor that enables tools to debug Edge using the CDP.

## Using DevTools frontend with other platforms

#### Android
- [Facebook Stetho](https://github.com/facebook/stetho) - Native Android debugging with Chrome DevTools.
- [j2v8-debugger](https://github.com/AlexTrotsenko/j2v8-debugger) - Debugging JavaScript running in [J2V8](https://github.com/eclipsesource/J2V8) with Chrome DevTools.

#### ClojureScript
- [Dirac](https://github.com/binaryage/dirac) - Debugging of ClojsureScript.

#### Lua
- [Mare](https://github.com/muzuiget/mare) - Lua debugging with Chrome DevTools.

#### iOS
- [PonyDebugger](https://github.com/square/PonyDebugger) - Remote network and data debugging iOS apps with Chrome DevTools.

#### Go
- [go-debugger-devtools](https://github.com/allada/go-debugger-devtools)

#### Node.js
- [ndb](https://github.com/GoogleChromeLabs/ndb) - An improved Node.js debugging experience with the DevTools Frontend.
- [Debugging Node.js with Chrome DevTools](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27) - Guide on using the full debugging and profiling support in Node v6.3+.
- [thetool](https://github.com/sfninja/thetool) - CPU, memory, coverage, type profiling with Node.


---

## DevTools Extensions

### Accessibility (A11y)
- [Chromelens](http://chromelens.xyz) - See how your web app will look to people with different types of vision and the path users will travel when tabbing through your page.

### Workflow
- [Clockwork](https://chrome.google.com/webstore/detail/clockwork/dmggabnehkmmfmdffgajcflpdjlnoemp?hl=en) - View PHP application profiling data.
- [Emulated Device Lab](https://chrome.google.com/webstore/detail/emulated-device-lab/oaonfodocibcdobdeelbbfggjombamff) - Experiment with multiple devices being emulated at the same time.
- [RailsPanel](https://chrome.google.com/webstore/detail/railspanel/gjpfobpafnhjhbajcjgccbbdofdckggg?hl=en-US) - View Ruby on Rails application profiling data.
- [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) - Inspect the React component hierarchies.
- [EmberJS Inspector](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi) - Allows you to inspect EmberJS objects in your application.
- [VueJS Developer Tools](https://github.com/vuejs/vue-devtools) - Inspect VueJS components and manipulate their data.
- [Angular Batarang](https://chrome.google.com/webstore/detail/angularjs-batarang/ighdmehidhipcmcojjgiloacoafjmpfk) - Inspect an Angular application's scope and profile its data.
- [Augury](https://augury.angular.io) - Debugging and Profiling for Angular 2 applications.
- [Marionette Inspector](https://chrome.google.com/webstore/detail/marionette-inspector/fbgfjlockdhidoaempmjcddibjklhpka) - Inspect a Marionette application's views, events, and live data.
- [Backbone Debugger](https://chrome.google.com/webstore/detail/backbone-debugger/bhljhndlimiafopmmhjlgfpnnchjjbhd) - Inspect a Backbone application's views, models, events, and routes.
- [App Inspector for Sencha](https://chrome.google.com/webstore/detail/app-inspector-for-sencha/pbeapidedgdpniokbedbfbaacglkceae) - Inspect a Sencha ExtJS/Touch application's component tree, data stores, events, and layouts.
- [Redux Devtools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) - Inspect Redux with actions history, undo and replay.
- [Three.js](https://chrome.google.com/webstore/detail/threejs-editor-extension/fbgbekpggeldiacgjkacbkkcbjhmakea/) - Edit any three.js project.
- [Insight](https://github.com/3Dparallax/insight/) - A WebGL debugging toolkit which enables more productive WebGL development and more efficient WebGL applications.
- [BEM devtools](https://github.com/escaton/bem-chrome-devtools) - Inspect BEM entities expressed in `i-bem` framework.
- [Metal.js Developer Tools](https://chrome.google.com/webstore/detail/metaljs-developer-tools/fagnjmppkokolnbloalifcmcooldhiik) - Inspect the Metal component hierarchies.

### UX
- [DevTools Author](https://chrome.google.com/webstore/detail/devtools-author/egfhcfdfnajldliefpdoaojgahefjhhi) - A selection of themes to modify parts of DevTools related to authoring web applications.
- [Zero Dark Matrix](https://chrome.google.com/webstore/detail/devtools-theme-zero-dark/bomhdjeadceaggdgfoefmpeafkjhegbo) - Dark theme for Chrome Developer Tools.

### Performance
- [Chrome React Perf](https://chrome.google.com/webstore/detail/react-perf/hacmcodfllhbnekmghgdlplbdnahmhmm) - An Operation Interface for react-addons-perf Package.
- [sloth](https://github.com/denar90/sloth) - Chrome extension allows to enable and save CPU and network throttling for selected tabs.

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

This awesome list is licensed into the Public Domain under Creative Commons 0. For more information please see the [license](LICENSE) file.

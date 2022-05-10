## react-three-fiber / single-spa error investigation
### environment
Firefox v99.0.1 (demo fails to render in other browsers, but less helpful error messaging is provided)
### replication steps
1. clone repo to your local device
2. run `npm i`
3. run `npm start -- --port 8500`
4. open single-spa-playground.org/playground/instant-test?name=@net-project/react-net&url=8500
5. observe the error outlined below

once the single-spa-playground is launched, browser performance will start to slow and a banner will eventually appear asking if you'd like to stop the page from slowing down the browser. after pressing "Stop", the following error (truncated) appears in the browser console:


```
Script terminated by timeout at:
handleError@http://localhost:8500/net-project-react-net.js:18368:25
renderRootSync@http://localhost:8500/net-project-react-net.js:18482:18
performSyncWorkOnRoot@http://localhost:8500/net-project-react-net.js:18069:18
workLoop@http://localhost:8500/net-project-react-net.js:24132:42

...

systemJSPrototype.import/<@https://cdn.jsdelivr.net/npm/systemjs/dist/system.js:231:24
promise callback*systemJSPrototype.import@https://cdn.jsdelivr.net/npm/systemjs/dist/system.js:229:6
systemJSPrototype.import@https://cdn.jsdelivr.net/npm/systemjs/dist/system.js:779:19
@http://single-spa-playground.org/:106:16
react-reconciler.development.js:15120
```

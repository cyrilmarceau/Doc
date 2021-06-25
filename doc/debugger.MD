# Debugger Reactotron for React and React native
## Installation
Dowload desktop app [Reactotron](https://github.com/infinitered/reactotron/releases/tag/v2.17.1)

```js
$ npm i --save-dev reactotron-react-native
```

## Project folder
- Create ReactotronConfig.js
> With EXPO: `-ipAdress` is below connection
```js
import Reactotron from 'reactotron-react-native'

if (__DEV__) {
    Reactotron.configure({ host: 'ipAdress' }).useReactNative().connect()
    Reactotron.clear()
    // Running on android device
    // $ adb reverse tcp:9090 tcp:9090
    Reactotron.clear()
    console.warn = Reactotron.log
    console.log = Reactotron.log
}
```

```js
App.js

import('./ReactotronConfig')
import Reactotron from 'reactotron-react-native'
```
## Start your app
- ##### Launch the reactotron application
- ##### Start your expo app
- ##### Now your logs appear in Timeline in Reactotron App
- > If the app is not load: `RELOAD YOUR APP AND THE LOGS WILL APPEAR` 
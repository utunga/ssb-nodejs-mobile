# Scuttlebot on nodejs-mobile

Experimentation for running [scuttlebot](https://github.com/ssbc/scuttlebot) with [nodejs-mobile-react-native](https://github.com/janeasystems/nodejs-mobile-react-native).

## Goals

- proof-of-concept Android :white_check_mark:
- proof-of-concept iOS :white_check_mark:
- support more native modules (sodium, leveldown, utp-native) :x:

## Installation 

```
git clone https://github.com/luandro/ssb-nodejs-mobile.git
cd ssb-nodejs-mobile
npm i
```

Than open the project's `./android` directory in Android Studio in order to download all the necessary dependencies.

Next, enter the `nodejs-assets/nodejs-project` directory and run `npm install` which will also run `npm run prepare` to patch `nodejs-mobile-react-native`.

`npm run dev` to start Android development and logging.

Use `adb logcat -s "NODEJS-MOBILE"` to log NodeJS application.

## Fixes that made this possible
- [Scuttlebot fork](https://github.com/luandro/scuttlebot) (uses [chloride](https://github.com/dominictarr/chloride) instead of [sodium-native](https://github.com/sodium-friends/sodium-native))
- [NodeJS Mobile - name collision error](https://github.com/janeasystems/nodejs-mobile/issues/34#issuecomment-358142287)
- [NodeJS Mobile - folders starting with underscore not copied on Android](https://github.com/janeasystems/nodejs-mobile/issues/60#issuecomment-381288106)

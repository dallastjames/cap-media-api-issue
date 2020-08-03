# Missing Cordova Resources Example Project

XCode gives the following error at build time using this project:

> 'Cordova/CDVPlugin+Resources.h' file not found

## Steps To Replicate Issue

### Using This Project

- `git clone` this Project
- `npm i`
- `npm run build`
- `npx cap sync ios`
- `npx cap open ios`
- Attempt to build using XCode

### Using a new Project

- Create a new Capacitor Project
- `npm run build && npx cap add ios`
- Add the following plugins
  - `cordova-plugin-iosrtc`
  - `phonegap-plugin-media-recorder`
  - `cordova-plugin-file`
  - `es6-promise-plugin`
- Follow the `Bridging Header` and `CocoaPods` steps in the guide here: https://github.com/cordova-rtc/cordova-plugin-iosrtc/blob/master/docs/Building.md
- Add the required permissions for the plugin
- `npx cap sync ios`
- `npx cap open ios`
- Attempt to build using XCode

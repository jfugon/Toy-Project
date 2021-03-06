# WebdriverIO-V7-appium-cucumber-boilerplate

Boilerplate project to run native and browser for android and ios using cucumber with page object pattern.

## Based on

- [WebdriverIO v7](https://webdriver.io/docs/gettingstarted)
- [Cucumber v7](https://cucumber.io/docs/cucumber/)
- [Node version 10.16 or higher](https://nodejs.org/es/)
- [Appium](https://appium.io/docs/en/about-appium/intro/)

## Supports
- Native Android and iOS apps
- Android Chrome browser 
- iOS Safari browser 
- Supports Page Object Model
- Contains sample test scenarios in cucumber
- Supports multiple cucumber html reports

## Source
Click below to know more 
- [Appium Introduction](http://appium.io/docs/en/about-appium/intro/)
- [Appium Capabilities](http://appium.io/docs/en/writing-running-appium/caps/)
- [Running Appium Tests](http://appium.io/docs/en/writing-running-appium/running-tests/)

## Running sample test
Follow the below commands: -

- Install dependencies using `npm i` in the terminal.
- Install appium globally on your PC: `npm install -g appium`
- Export Android and Java environment variables

```bash
export JAVA_HOME=$(/usr/libexec/java_home)
export ANDROID_HOME=/Users/YOUR_USER/Library/Android/sdk
export ANDROID_SDK_ROOT=/Users/YOUR_USER/Library/Android/sdk
export ANDROID_AVD_HOME=/Users/YOUR_USER/.android/avd
export HTTP_PROXY=myserver:1981
export PATH="$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools:$PATH"

```

- Save your exports

```bash
source ~/.zshrc
```

- Update the deviceName and platFormVersion in `config/android.info.js` and `config/ios.info.js` respectively.

- Execute `npm run iosApp` to run ios native app

- Execute `npm run iosBrowser` to run ios safari browser

- Execute `npm run androidApp` to run android native app

- Execute `npm run androidBrowser` to run android chrome browser

- Execute `npm run lint` to run eslint

## Setting up WDA for Running tests on IOS Real devices
- Download and Install appium Desktop on your PC

- Install appium globally on your PC: `npm install -g appium`

- You can follow the steps in this link: http://appium.io/docs/en/drivers/ios-xcuitest-real-devices/#basic-manual-configuration

- Or follow these ones (Almost the same as the link posted above):

- Create an Apple Developer ID with your account (Ask the IOS Team for help in this one)

- Download the Apple Developer ID Certificate and install it on your MAC

- Install Xcode on your MAC

- Connect IOS device to the PC

- Open the WDA project in Xcode. For this, go to: Applications/Appium.app/Contents/Resources/app/node_modules/appium/node_modules/appium-webdriveragent

- Open the "WebDriverAgent.xcodepro" 

- On the Targets displayed on Xcode select "WebDriverAgentLib" and Select the "Signing and Capabilities" tab

- Check the "Automatically manage signing" checkbox

- Select "Escolarea LLC" on the Team dropdown list

- Select "Development" on the Signing Certificate dropdown list

- Click on the "Build" project button in the Xcode Navbar and wait for the project to build successfully

- Repeat these last 5 steps for the "WebDriverAgentRunner" Target

- Once the "WebDriverAgentRunner" Target is build successfully on XCode, select the "Product" tab on Xcode bar

- Click the "Test" button and wait for the WDA to be installed on the IOS Device

- Once the WDA is installed, you can run the IOS tests successfully. Refer to the "Running sample test" Section of this README 

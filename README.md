# stac2021
- This repo includes sample code for demonstration on TBD, Software Test Automation Conference 2021(Japanese).
- The slide: TBD
- The movie: TBD

## Preparation
1. Prepare `npm` and `node`
    ```
    # In my case
    $ node -v
    > v12.13.1
    $ npm -v
    > 6.12.1
    ```
2. Run commands as 
    ```
    $ cd appium1.x
    $ npm install
    $ cd appium2.0
    $ npm install
    ```
3. Update line 21 of appium1.x/test_android.js as you need 

## How to kick sample test scirpt
1. Start an Android emulator (in my case API 29)
2. Start an appium server
    ```
    # When Appium 1.x
    $ cd appium1.x
    ./node_modules/.bin/appium
    # When Appium 2.0
    $ cd appium2.0
    $ ./node_modules/.bin/appium driver install uiautomator2
    $ ./node_modules/.bin/appium plugin install --source=npm @appium/relaxed-caps-plugin
    $ ./node_modules/.bin/appium --base-path /wd/hub --use-plugins=relaxed-caps
    ```
3. Launch another terminal, and start a test script
    ```
    $ cd appium1.x
    $ node test_android.js
    ```


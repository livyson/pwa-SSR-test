## *pwa-ssr-testing*


It is our automation project that aims to open CHROME and FIREFOX browsers with javascript disabled.
This project will soon be used to test the page in a browser used for Google SSR.

The next steps for this project are:
* Run rendering tests of QuintoAndar pages using the browser configured (javascript disabled)
* Point the current test in CI to open in Chrome Chromium Version 41.0.2272.0 custom (64-bit)
* Do not allow the build to generate a version if the SSR test is broken

## *SETUP*

Install a framework to allow us to work with Selenium from inside Node:
```shell
npm install selenium-webdriver
```

Set your PATH variable:
```shell
export PATH=$PATH:/Users/<user>
```

Check that your new paths are in the PATH variable by entering the following into your terminal:
```shell
echo $PATH
```

Install *geckodriver* to provides the HTTP API described by the WebDriver protocol to communicate with Gecko browsers, such as Firefox. It translates calls into the Firefox remote protocol by acting as a proxy between the local- and remote ends:

Download the latest version:
```shell
wget https://github.com/mozilla/geckodriver/releases/download/v0.18.0/geckodriver-v0.18.0-linux64.tar.gz
```

Extract the file with:
```shell
tar -xvzf geckodriver*
```

Make it executable:
```shell
chmod +x geckodriver
```

Add the driver to your PATH so other tools can find it:
```shell
export PATH=$PATH:/path-to-extracted-file/geckodriver
```

To update the npm packages:
```shell
npm install
```

## *RUN*

To run the file that open the Firefox with javascript disabled:
```shell
node access_landing_page_by_firefox_test.js           // if that does not work, try without the extension js
```

To run the file that open the Chrome with javascript disabled:
```shell
node access_landing_page_by_chrome_test.js           // if that does not work, try without the extension js
```

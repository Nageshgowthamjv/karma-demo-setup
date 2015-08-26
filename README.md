# karma-demo-setup
Demo setup for karma which can be cloned and directly used. 

### What is karma-demo-setup?
This is a sample set up configuration for setting up the Karma test runner. This can be directly cloned or downloaded directly to make use of it.

### How to setup an instance?
Once it is downloaded, install it using npm.

`npm install`

### where to write test cases?
All the JavaScript files inside the folder "tests" are currently considered as test files. We can configure test file Location as well as test file pattern in the configurations.

`files: [
    'tests/*.js'
]`

### How to configure browsers for testing?
  To Run test cases in the different browsers, First we need all those browsers installed in the System. Then node requires launching software for launching the each browser. Examples are `karma-chrome-launcher`, `karma-firefox-launcher`, `karma-phantomjs-launcher` etc... These are registered inside `package.json` file. so when `package.json` is installed, dependencies are automatically downloaded into the instance. 
  
  For testing we can register browsers in the `browsers: ['PhantomJS', 'Chrome', 'Firefox']` config.
  
### What are the testing frameworks used here?
  `Mocha` and  `Chai`.
  
### Sample Config.
```
config.set({
        basePath: '',
        frameworks: ['mocha', 'chai'],
        files: [
            'tests/*.js'
        ],
        reporters: ['mocha'],
        port: 9876,
        colors: true,
        autoWatch: false,
        singleRun: true,
        // level of logging
        // possible values: config.LOG_DISABLE || config.LOG_ERROR || config.LOG_WARN || config.LOG_INFO || config.LOG_DEBUG
        logLevel: config.LOG_INFO,
        //browsers: ['PhantomJS', 'Chrome', 'Firefox']
        browsers: ['PhantomJS']
    });
```
### Dependencies
```
"devDependencies": {
    "chai": "^2.3.0",
    "grunt-mocha": "^0.4.12",
    "karma": "^0.12.31",
    "karma-chai": "^0.1.0",
    "karma-chrome-launcher": "^0.1.12",
    "karma-firefox-launcher": "^0.1.6",
    "karma-mocha": "^0.1.10",
    "karma-mocha-reporter": "^1.0.2",
    "karma-phantomjs-launcher": "^0.1.4",
    "karma-spec-reporter": "0.0.19",
    "mocha": "^2.2.4"
  }
```

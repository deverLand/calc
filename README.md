# Jest testing session 1

## What is Jest?
**Jest** is an open source library for testing JavaScript code. It is a project maintained and created by Facebook engineers for its *React* project. Its strengths are:

 * it’s fast
 * it can perform snapshot testing
 * it’s opinionated, and provides everything out of the box without requiring you to make choices

Jest is a tool very similar to Mocha, although they have differences:

 * Mocha is less opinionated, while Jest has a certain set of conventions
 * Mocha requires more configuration, while Jest works usually out of the box, thanks to being opinionated
 * Mocha is older and more established, with more tooling integrations

## Setup, Test Procedure Overview

 1. Jest requires *nodejs* to be installed.
 2. Jest installed in a project or globally via *yarn* or *npm*
 3. [Optional/Recommended] Update *package.json*
 4. Create test file with format: **.test.js*
 5. Run test via:
    * *yarn test* or *npm test*
    * *yarn test [*.test.js]* or *npm test [*.test.js]*


## Step-by-step
1. Not in the scope of this tutorial.

2. Jest is automatically installed in ```create-react-app```, so if you use that, you don’t need to install Jest.

Jest can be installed in any other project using *Yarn*:

```yarn add --dev jest```
```yarn global add jest```

or through *npm*

node _v8: 
```npm install --save-dev jest [--global]```

node _v12: 
```npm i --only=dev jest [--global]```

3. Add to your *package.json* this line:
```json
"scripts": { 
    "test": "jest [--verbose]", 
    ... 
}```

4. Write the test script. Normally, there are three (3) parts in a test script:
    1. import <module_files>
    2. describe('module')
    3. test (TDD) or it (BDD)
    4. test script
    
## Notes
by default, jest runs all js files inside __test__ folder
mocks are off by default, jest will search mock files in __mockes__
jest saves all snapchats inside __snapshots__
jest can run test inside a fake DOM implementation

additional params on run: 
```jest --watch```
```jest --coverage```

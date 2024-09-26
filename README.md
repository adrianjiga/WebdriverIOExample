# WebdriverIO Automation Project

This project uses WebdriverIO for automated testing of web applications. It provides a basic setup for running tests using the Mocha framework and Chrome browser.

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v12 or higher)
- npm (usually comes with Node.js)
- Google Chrome browser

## Setup

1. Clone this repository:

   ```
   git clone https://github.com/adrianjiga/WebdriverIOExample
   cd WebdriverIOExample
   ```

2. Install dependencies:
   ```
   npm install
   ```

## Project Structure

- `package.json`: Node.js project file with scripts and dependencies

## Running Tests

To run all tests:

```
npm test
```

This command will execute all test files in the `test/specs/` directory.

## Writing Tests

1. Create new test files in the `test/specs/` directory with a `.js` extension.
2. Use the Mocha framework syntax for writing tests.
3. Utilize WebdriverIO commands for browser interactions.

Example test structure:

```javascript
describe('My Feature', () => {
  it('should do something', async () => {
    await browser.url('https://example.com');
    await $('#element-id').click();
    await expect($('#result')).toHaveText('Expected Result');
  });
});
```

## Configuration

The `wdio.conf.js` file contains the WebdriverIO configuration. Modify this file to:

- Change the browser or add multiple browsers
- Adjust timeouts
- Add plugins or reporters
- Configure parallel execution

## Troubleshooting

If you encounter issues:

1. Ensure all dependencies are correctly installed.
2. Check that Chrome browser is up to date.
3. Verify that the application under test is accessible.
4. Review WebdriverIO logs for detailed error messages.

## Resources

- [WebdriverIO Documentation](https://webdriver.io/docs/gettingstarted)
- [Mocha Documentation](https://mochajs.org/)
- [Chai Assertion Library](https://www.chaijs.com/)

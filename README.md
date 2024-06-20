### Categories

#### Test Automation Best Practices
- **What is a key benefit of writing end to end tests?**
  - Ensuring Application Functionality from the user’s perspective is working correctly
  
- **What is it to isolate a system under test by replacing a real dependency such as APIs with a controlled replacement, allowing reliable and faster tests?**
  - Mocking
  
- **How does parallel test execution improve the efficiency of end to end tests?**
  - Reduce overall test run time and making better use of available resources
  
- **Why should automated tests be idempotent?**
  - Ensure tests can be run independently and consistently without being affected by previous run times. Makes debugging easier and prevents cascading failures.
  
- **What are some reasons that we should run E2E tests in our CI systems? At least three**
  - Early detection of issues
  - Ensure existing functionality is not broken
  - Automated Execution
  - Consistent Environment
  - Visibility
  - Stable and reliable releases
  - Simulate user interaction providing test coverage w/ unit / integration tests

#### Playwright Architecture
- **What is it in playwright when it performs a range of actionability checks on elements before making actions to ensure the actions behave as expected?**
  - Auto-Waiting Feature
  
- **Why does Playwright use browser context, and what problem do they solve?**
  - Create an isolated, concurrent browser session within a single browser instance, solving the problem of test interference
  
- **Why is it important to use ‘await’ when interacting with elements in Playwright tests?**
  - Ensure each step completes before moving on to the next, maintaining the correct order of operations
  
- **How does Playwright achieve consistent test results across different browsers?**
  - Providing a unified API for chromium, firefox, and webkit, allowing tests to run identically across these browsers
  
- **Cypress uses a custom injected library in the browser that takes control of the execution of your code. In playwright, who’s in control? Provide the name and a brief description of what it is**
  - A: Chrome DevTools Protocol is a set of high-level APIs that allows developers to communicate with chromium-based browsers

#### Playwright Core Concepts
- **What is Playwright primarily used for in web development?**
  - End to End Testing
  
- **Playwright uses a ___ mechanism to reduce test flakiness by reducing the impact of transient issues on test results. This mechanism is primarily seen with expect() assertions**
  - Auto-Retrying
  
- **What is the advantage of using fixtures in playwright tests?**
  - Providing consistent and isolated environment for tests, reducing dependencies and flakiness
  
- **What are the three advantages of using web first assertions?**
  - Better error handling, simplified test code, and reduced flakiness
  
- **Playwright splits the process of showing a new document in a page by navigation and loading. For the loading section, fill in the blank for the remaining four**
  - (GIVEN) Page.url() is set to the new url
  - Document content is loaded over network and parsed
  - Page.on('documentcontentloaded') event is fired
  - Page executes scripts and loads resources like stylesheets and images
  - (GIVEN) Page.on('load') event is fired
  - Page executes dynamically loaded scripts

#### Playwright Testing 1
- **What is the primary function used to declare an assertion in playwright?**
  - Expect()
  
- **What is the primary function used to mock and modify network traffic in Playwright?**
  - Page.route or route
  
- **Page Object Models are used to ____ which improves ____**
  - To abstract Interactions within a page which improves test readability and maintainability
  
- **What are the three additional testing possibilities I’ve explored in this presentation on playwright?**
  - Websocket testing
  - Visual Comparisons with screenshots
  - Android/Android Webview Testing
  
- **Describe the process in which we can eliminate the need to authenticate every test in Playwright.**
  - Utilize an authentication route that will produce an authenticated browser state that we can save to a file locally. Tests will then reuse this state and start authenticated

#### Playwright Testing 2
- **____ is a central piece of playwright’s auto-waiting and retry-ability which primarily represents a way to find elements on a page.**
  - Locators
  
- **Which Built-In Fixture is responsible for managing and interacting with individual web page? This is one of the most commonly used fixture for playwright tests.**
  - Page
  
- **Playwright uses ___ to create an isolated concurrent browser session within a single browser instance to solve the problem of test interference.**
  - BrowserContext
  
- **What are the three ways that we can approach debugging in Playwright?**
  - Debug mode in Visual Studio Code & breakpoints
  - Trace Viewer and UI Mode
  - Chrome DevTools, console by enabling PWDebug
  
- **What are the four built-in test fixtures available for Playwright?**
  - Browser
  - BrowserContext
  - Page
  - Request

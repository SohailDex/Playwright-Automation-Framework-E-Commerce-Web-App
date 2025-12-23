name: Playwright Automation Tests  
  
on: [push, pull_request]  
  
jobs:  
  test:  
    runs-on: ubuntu-latest  
    steps:  
      - uses: actions/checkout@v3  
      - uses: actions/setup-node@v3  
      - run: npm install  
      - run: npx playwright install  
      - run: npm test  

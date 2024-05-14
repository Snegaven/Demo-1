on:
  push:
    branches: [demo-1]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2

      - name: Install Dependencies
        run: npm install

      - name: Build
        run: npm run build

      - name: Test
        run: npm test

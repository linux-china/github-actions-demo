GitHub Actions demo
==========================
Simple Node.js application to demonstrate the use of GitHub Actions

# act quickstart

Try these:

* `act -j test` - run the tests
* `act` - run the the entire pipeline
* `act -l` - view the execution graph

# Setup dotenvx

Please add `uses: linux-china/setup-dotenvx@main` to your workflow file to set up dotenvx CLI.

```yaml

dotenvx-demo:
  runs-on: ubuntu-latest
  steps:
    - uses: actions/checkout@v4
    - uses: linux-china/setup-dotenvx@main
    - run: npm install
    - run: dotenvx run -- node index.js
```

# References

* [act](https://github.com/nektos/act): Run your GitHub Actions locally

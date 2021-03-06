# nextjs-truffle-tailwindcss-boilerplate
 
This boilerplate comes with everything you need to start using smart contracts from a Nextjs-tailwindcss app. This is as barebones as it gets, so nothing stands in your way.

## Installation

First ensure you are in a new and empty directory.

1. Run the `git clone https://github.com/paschal533/next-truffle-tailwindcss-boilerplate.git`. This will install all necessary dependencies. A Nextjs-tailwindcss is generated in the root directory, and a Solidity-truffle contract is generated in the Smart_contract directory.
   ```
   git clone https://github.com/paschal533/next-truffle-tailwindcss-boilerplate.git
   ```

- ## Run the development console.
 Cd into the Smart_contract directory and run
    ```javascript
    truffle develop
    ```

- Compile and migrate the smart contracts. Note inside the development console we don't preface commands with `truffle`.
    ```javascript
    compile
    migrate
    ```

- In the `root` directory, we run the Nextjs app. Smart contract changes must be manually recompiled and migrated.
    ```javascript
    // in another terminal (i.e. not in the truffle develop prompt)
    npm run start
    ```

- Truffle can run tests written in Solidity or JavaScript against your smart contracts. Note the command varies slightly if you're in or outside of the development console.
    ```javascript
    // inside the development console.
    test

    // outside the development console..
    truffle test
    ```

- Jest is included for testing React components. Compile your contracts before running Jest, or you may receive some file not found errors.
    ```javascript
    // ensure you are inside the client directory when running this
    npm run test
    ```

- To build the application for production, use the build script. A production build will be in the `.next` folder.
    ```javascript
    // ensure you are inside the client directory when running this
    npm run build
    ```

## FAQ

* __How do I use this with the Ganache-CLI?__

    It's as easy as modifying the config file! [Check out our documentation on adding network configurations](http://truffleframework.com/docs/advanced/configuration#networks).

* __Where is my production build?__

    The production build will be in the `.next` folder after running `npm run build` in the `root` folder.

* __Where can I find more documentation?__

    This boilerplate is a marriage of [Truffle](http://truffleframework.com/) and a Nextjs setup created with [create-nextjs-app](https://nextjs.org/docs). Either one would be a great place to start!

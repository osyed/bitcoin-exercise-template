# bitcoin-exercise-template

## Getting Started

### Repository Setup

1. Clone this repo into `bitcoin-exercise-[YOUR_NAME]`:

	`git clone --recurse-submodules https://github.com/osyed/bitcoin-exercise-template.git bitcoin-exercise-[YOUR_NAME]`

2. Open a git terminal in the repo and run the following commands:

	`git remote set-url origin https://github.com/osyed/bitcoin-exercise-[YOUR_NAME].git`

### Installing NPM Packages

1. Use `npm install --save ...` like normal to install packages as necessary for each exercise.

	*NOTE: Do not remove pre-existing dependencies from the 'package.json' file. Add additional dependencies to the same 'package.json' file.*

### Running Tests

The `test/` folder is a git submodule pointing to the [osyed/bitcoin-exercise-tests](https://github.com/osyed/bitcoin-exercise-tests.git) repository.

The `test/` submodule has branches for each of the exercises:

* ex1
* ex2
* ex3
* ex4
* ex5
* ex6
* ex7

When you make a branch for an exercise, set the `test/` submodule to get the right tests with:

`git submodule update --remote`

Once you have pulled the tests, commit, and run them with:

`npm test`

#### Auto-checkout tests when changing branches

To make git automagically pull the right tests when you checkout a branch, use:

`git checkout <branch> --recurse-submodules`

_Note: This will use a cached version of the tests. To get latest run:  
`git submodules update --remote`_

_Note: Make life easy, get git >= 2.14 and set:  
`git config --global submodule.recurse true`  
to make this happen by default._

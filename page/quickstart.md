Title: Yesod quick start guide

## Try it online

[FP Haskell Center](https://www.fpcomplete.com/business/haskell-center/overview/)
provides a web based development environment with all of the
Haskell toolchain and Yesod libraries preinstalled. You can get started right
away by [cloning an existing Yesod
project](https://www.fpcomplete.com/school/project-templates/file-server).

## Local installation

To use Yesod on your local system, you'll need to [install the Haskell
toolchain](http://www.stackage.org/install). Once you have Haskell installed, you can follow these steps to get a scaffolded site up and running:

The simplest set of steps to get this started is:

1. Create a new directory to hold your project, and `cd` into it
2.  Run the following series of commands

    ```shell
    wget http://www.stackage.org/lts/cabal.config
    cabal update                       # download package list
    cabal install alex happy yesod-bin # install build tools
    yesod init --bare                  # answer questions as prompted
    cabal sandbox init                 # set up a sandbox
    cabal install --run-tests          # install libraries
    yesod devel                        # launch devel server
    ```

3. View your Yesod site at [http://localhost:3000/](http://localhost:3000/)

These steps download some necessary tools, create a scaffolded site, set up a
sandbox, and install all libraries. Note that it may take some time to compile
all dependencies. These steps also leverage
[Stackage](http://www.stackage.org/) to ensure you have a consistent library
set and avoid "cabal hell" issues, which came up in the past.

### System libraries

Note that you will need the dev version of some system libraries to be
available for the above steps to work. For example, on Ubuntu, you may need to
run something like:

    sudo apt-get install -y build-essential zlib1g-dev

If you're using a database, you'll likely need to install the system libraries
to talk to it. Some Ubuntu examples are:

    sudo apt-get install -y libmysqlclient-dev
    sudo apt-get install -y libpg-dev

## Learn more

Now it's time to start coding! You can play around with the code right now, or
if you want to learn more, check out these resources:

* [Yesod book](/book)
* [Community](/page/community)
* [Yesod tutorial](http://yannesposito.com/Scratch/en/blog/Yesod-tutorial-for-newbies/)
* [The Wiki](/wiki)
* [Screencasts](/page/screencasts)

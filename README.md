Sexcore Node
============

[![NPM Package](https://img.shields.io/npm/v/sexcore-node.svg?style=flat-square)](https://www.npmjs.org/package/sexcore-node)
[![Build Status](https://img.shields.io/travis/Sxcmarket/sexcore-node.svg?branch=master&style=flat-square)](https://travis-ci.org/Sxcmarket/sexcore-node)
[![Coverage Status](https://img.shields.io/coveralls/Sxcmarket/sexcore-node.svg?style=flat-square)](https://coveralls.io/r/Sxcmarket/sexcore-node)

A Sexcoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to [Sexcoin Core with additional indexing](https://github.com/Sxcmarket/sexcore-sexcoin) for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Install

```bash
npm install -g sexcore-node
sexcore-node start
```

Note: For your convenience, we distribute bitcoind binaries for x86_64 Linux and x86_64 Mac OS X. Upon npm install, the binaries for your platform will be downloaded. For more detailed installation instructions, or if you want to compile the project yourself, then please see the Bitcore branch of [Sexcoin Core with additional indexing](https://github.com/Sxcmarket/sexcore-sexcoin).

## Prerequisites

- GNU/Linux x86_32/x86_64, or OSX 64bit *(for bitcoind distributed binaries)*
- Node.js v0.10, v0.12 or v4
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~200GB of disk storage
- ~8GB of RAM

## Configuration

Sexcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Sexcore Node.

```bash
sexcore-node create -d <bitcoin-data-dir> mynode
cd mynode
sexcore-node install <service>
sexcore-node install https://github.com/yourname/helloworld
```

This will create a directory with configuration files for your node and install the necessary dependencies. For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/Sxcmarket/insight-sexcoin-api)
- [Insight UI](https://github.com/Sxcmarket/insight-sexcoin-ui)
- [Sexcore Wallet Service](https://github.com/Sxcmarket/sexcore-wallet-service)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## Contributing
Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/Sxcmarket/sexcore/blob/master/CONTRIBUTING.md) file.


## License

Code released under [the MIT license](https://github.com/Sxcmarket/sexcore-node/blob/master/LICENSE).

Copyright 2016 The Litecoin Core Developers
Copyright 2017 The Sexcore Core Developers

- bitcore: Copyright (c) 2013-2015 BitPay, Inc. (MIT License)
- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)

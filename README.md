Bitcore Node Zcoin
============

A Zcoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to [Zcoin Core v0.13.4.x](https://github.com/zcoinofficial/zcoin/tree/v0.13.4.3) for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Prerequisites

- Zcoin Core (v0.13.4.x) with support for additional indexing *(see above)*
- Node.js v0.10, v0.12, v4 or v5
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~20GB of disk storage
- ~1GB of RAM

## Configuration

Bitcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Bitcore Node.

```bash
bitcore-node-zcoin create -d <zcoin-data-dir> mynode
cd mynode
bitcore-node-zcoin install https://github.com/sn-ntu/insight-api-zcoin
bitcore-node-zcoin install https://github.com/sn-ntu/insight-ui-zcoin
bitcore-node-zcoin start
```

This will create a directory with configuration files for your node and install the necessary dependencies.

Please note that [Zcoin Core v0.13.4.x](https://github.com/zcoinofficial/zcoin/tree/v0.13.4.3) will be downloaded automatically. Once completed the zcoind binary should be placed into the &lt;zcoin-data-dir&gt; folder specified during node creation.

For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/sn-ntu/insight-api-zcoin/tree/master)
- [Insight UI](https://github.com/sn-ntu/insight-ui-zcoin/tree/master)

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

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) file.

## License

Code released under [the MIT license](https://github.com/sn-ntu/bitcore-node-zcoin/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2018 Bitcoin Core Developers (MIT License)
- zcoin: Copyright (c) 2016-2018 Zcoin Core Developers (MIT License)

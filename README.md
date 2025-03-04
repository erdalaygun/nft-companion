<p align="center">
  <a href="https://xch.gallery">
    <img src="https://xch.gallery/pflanz_128.png" alt="xch.gallery logo" width="128" height="128">
  </a>
</p>

<h3 align="center">NFT Companion</h3>

<div align="center">
  Create and trade NFTs on <a href="https://xch.gallery">xch.gallery</a> and the Chia blockchain.
</div>

## Installation

1. Clone the repository
```shell
git clone https://github.com/xch-gallery//nft-companion.git
cd nft-companion
```

2. Run the install script and activate the virtual environment
```shell
sh install.sh
. ./venv/bin/activate
```

## Create a new NFT singleton

The `create` command can be used to create a new NFT singleton using the Chia light wallet.
It requires a running wallet on your computer.

```shell
$ python3 nft.py create --help
Usage: nft.py create [OPTIONS]

Options:
  --name TEXT            The name of the NFT
  --uri TEXT             The uri of the main NFT image
  --fingerprint INTEGER  The fingerprint of the key to use [optional]
  --fee INTEGER          The XCH fee to use for this transaction  [default: 0]
  --help                 Show this message and exit.
```

The following example shows the creation of an example NFT singleton.

```shell
$ python3 nft.py create --name "Curly Nonchalant Marmot" --uri "https://example.com/curly-nonchalant-marmot.png" --fingerprint 2244856279
The transaction seems valid. Do you want to submit it? [y/N]: y
The NFT has been submitted successfully!
Please wait a few minutes for the NFT to be finalized.
You can inspect your NFT using the following link: https://xch.gallery/singletons/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## Attribution

The puzzles in this repository build on puzzles included in the [chia-blockchain](https://github.com/Chia-Network/chia-blockchain) project, which is licensed under Apache 2.0.

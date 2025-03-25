# Nerofea Network

Nerofea is a web3 water goddess. 

### A Sneak Peek Into My Projects

## NFN Proactive Voting for Sports, Live Entertainment and Local Council
Next-Step Action Voting, Merchandise Purchasing, and Proactive Interaction thanks to Pair Voting Mechanism Applied on Live-on-screen Engagement Tools
- Testing
- Conceptualizing
- Pitching
- Secret vs Public
- Rust-based, Substrate thinking
- Fast, real-time, proveability, and privacy-focused live-onscreen shopping feature

## Flare x Google Cloud Verifiable AI Hackathon
Technical Planning and Collaboration AI Tool for Planning Complicated Product Architectures & Discovery of Concept Development
– Designed and pitched an AI visual UML generator solution called (no name yet) to bridge the gap between NFN, Twitch, Telegram, and the complicated poltiical scape of cryptocurrencies and tokens. 
- Zero-sleep 48-hour hack. 
– Flare oracles
- Software Architecture
- API Configurations
--- Submitted on DOrahacks

## Flare EthOxford Hackathon (Oxford, Great Britain)
STORM Product Architecture & Concept Development
– Designed and pitched a solution called STORM to bridge the gap between NFN, Twitch, Telegram, and the complicated poltiical scape of cryptocurrencies and tokens. 
- Zero-sleep 48-hour hack. 
– Flare oracles
- Software Architecture, and API Configuration needs
-- Sponsored by friends and family

## Aztec Tribes (ZK Payment Requests) for the Aztec Hacker House (London, Great Britain)
– Created a dynamic Merkle tree system for modifiable payment approvals.
– Wrote smart circuits in Aztec Noir and Noir & scoped front and backend workflows.
- Discovery phase to discover centralized circuits vs Aztec Private State, PXE and auth-witness.
--- Sponsored by Aztec Labs / Aztec Foundation

## Aztec Empires (ZK Reporting Filing) for the Aztec Hacker House   (London, Great Britain)
– Created an append only Merkle tree system for finalizing financial and project reports.
– Wrote smart circuits in Aztec-Noir and Noir & scoped front and backend workflows.
- Discovery phase to discover centralized circuits vs Aztec Private State, PXE and auth-witness.
--- Sponsored by Aztec Labs / Aztec Foundation

## Polkadot Prodigy – 2nd Place, DeFi Category (Bulgaria)
Where the NFN and real-time concept was born. Where Nerofea discovered Rust and Substrate, the key to the final missing piece of the puzzle of the business concepts Nerofea believes the world needs and deserves. 
– Built a DeFi solution with automatic voting strategy and UI/UX flow.
– Created technical scope, user flows, and pitch script.
- Concept was backed by current consumer behavors. 
--- Sponsored by Polkadot Treasury
-- Submitted to Devpost

## 3D Shopping & Design Experience
Live Product & Design Simulation of 3D Room & Products for an Accurate Shopping Experience
– Immersive Three.js product scenes.
- WebGL Texture Loading
– COnfigurable with Twitch overlays
- ZK authentication receipt, usecasing NFN's functionality

## Belgrade Hackers League & TONBelgrade Hackathon (Serbia)
- Ideated TONPie Telegram App
- Architected the Booking and Payment Tool using NFN concepts using the TDlib Initializer 
- Scoped the live delivery tracking concept
--- Sponsored by Ivan Cholakov, Senior Software Engineer, Aventus Network

### Connect
💌 nerofea.offical@gmail.com  
💌 instagram.com/_nerofea
💌 twitch.com/nerofea
💌 twitter.com/nerofeaOfficial

### Helpful Docs (Resources for Beginner Builders)

- 📚 [Substrate Docs](https://docs.substrate.io/)  
- 🧱 [Aztec Noir Language Guide](https://noir-lang.org)  
- 🎨 [Three.js / WebGL Examples](https://threejs.org/examples/)  
- 🧠 [Polkadot/Substrate Ecosystem Explorer](https://substrate.dev/en/ecosystem)  
- 🧪 [ZK Hack Challenges](https://zkhack.dev/challenges/)  

### 🌱 Ideas I'm Exploring

- Decentralized governance through product UX  
- Privacy-preserving shopping and social commerce  
- Twitch-native auctions powered by smart contracts  
- Visual dev tools for AI-assisted product design  
- Real-time voting flows for live entertainment  

Most of these tie into NFN (Nerofea Functionality Network) — a modular vision I’m prototyping one repo at a time.

## Getting Started with NFN (not complete, below is draft from Cargo/Substrate)

Depending on your operating system and Rust version, there might be additional
packages required to compile this template. Check the
[Install](https://docs.substrate.io/install/) instructions for your platform for
the most common dependencies. Alternatively, you can use one of the [alternative
installation](#alternatives-installations) options.

```sh
cargo build --release
```

```sh
./target/release/node-template -h
```

You can generate and view the [Rust
Docs](https://doc.rust-lang.org/cargo/commands/cargo-doc.html) for this template
with this command:

```sh
cargo +nightly doc --open
```

The following command starts a single-node development chain that doesn't
persist state:

```sh
./target/release/node-template --dev
```

To purge the development chain's state, run the following command:

```sh
./target/release/node-template purge-chain --dev
```

To start the development chain with detailed logging, run the following command:

```sh
RUST_BACKTRACE=1 ./target/release/node-template -ldebug --dev
```

Development chains:

- Maintain state in a `tmp` folder while the node is running.
- Use the **Alice** and **Bob** accounts as default validator authorities.
- Use the **Alice** account as the default `sudo` account.
- Are preconfigured with a genesis state (`/node/src/chain_spec.rs`) that
  includes several prefunded development accounts.

To persist chain state between runs, specify a base path by running a command
similar to the following:

```sh
// Create a folder to use as the db base path
$ mkdir my-chain-state

// Use of that folder to store the chain state
$ ./target/release/node-template --dev --base-path ./my-chain-state/

// Check the folder structure created inside the base path after running the chain
$ ls ./my-chain-state
chains
$ ls ./my-chain-state/chains/
dev
$ ls ./my-chain-state/chains/dev
db keystore network
```

### Connect with Polkadot-JS Apps Front-End

After you start the node template locally, you can interact with it using the
hosted version of the [Polkadot/Substrate
Portal](https://polkadot.js.org/apps/#/explorer?rpc=ws://localhost:9944)
front-end by connecting to the local node endpoint. A hosted version is also
available on [IPFS (redirect) here](https://dotapps.io/) or [IPNS (direct)
here](ipns://dotapps.io/?rpc=ws%3A%2F%2F127.0.0.1%3A9944#/explorer). You can
also find the source code and instructions for hosting your own instance on the
[`polkadot-js/apps`](https://github.com/polkadot-js/apps) repository.

### Multi-Node Local Testnet

If you want to see the multi-node consensus algorithm in action, see [Simulate a
network](https://docs.substrate.io/tutorials/build-a-blockchain/simulate-network/).

## Template Structure

A Substrate project such as this consists of a number of components that are
spread across a few directories.

### Node

A blockchain node is an application that allows users to participate in a
blockchain network. Substrate-based blockchain nodes expose a number of
capabilities:

- Networking: Substrate nodes use the [`libp2p`](https://libp2p.io/) networking
  stack to allow the nodes in the network to communicate with one another.
- Consensus: Blockchains must have a way to come to
  [consensus](https://docs.substrate.io/fundamentals/consensus/) on the state of
  the network. Substrate makes it possible to supply custom consensus engines
  and also ships with several consensus mechanisms that have been built on top
  of [Web3 Foundation
  research](https://research.web3.foundation/en/latest/polkadot/NPoS/index.html).
- RPC Server: A remote procedure call (RPC) server is used to interact with
  Substrate nodes.

There are several files in the `node` directory. Take special note of the
following:

- [`chain_spec.rs`](./node/src/chain_spec.rs): A [chain
  specification](https://docs.substrate.io/build/chain-spec/) is a source code
  file that defines a Substrate chain's initial (genesis) state. Chain
  specifications are useful for development and testing, and critical when
  architecting the launch of a production chain. Take note of the
  `development_config` and `testnet_genesis` functions,. These functions are
  used to define the genesis state for the local development chain
  configuration. These functions identify some [well-known
  accounts](https://docs.substrate.io/reference/command-line-tools/subkey/) and
  use them to configure the blockchain's initial state.
- [`service.rs`](./node/src/service.rs): This file defines the node
  implementation. Take note of the libraries that this file imports and the
  names of the functions it invokes. In particular, there are references to
  consensus-related topics, such as the [block finalization and
  forks](https://docs.substrate.io/fundamentals/consensus/#finalization-and-forks)
  and other [consensus
  mechanisms](https://docs.substrate.io/fundamentals/consensus/#default-consensus-models)
  such as Aura for block authoring and GRANDPA for finality.

### Runtime

In Substrate, the terms "runtime" and "state transition function" are analogous.
Both terms refer to the core logic of the blockchain that is responsible for
validating blocks and executing the state changes they define. The Substrate
project in this repository uses
[FRAME](https://docs.substrate.io/learn/runtime-development/#frame) to construct
a blockchain runtime. FRAME allows runtime developers to declare domain-specific
logic in modules called "pallets". At the heart of FRAME is a helpful [macro
language](https://docs.substrate.io/reference/frame-macros/) that makes it easy
to create pallets and flexibly compose them to create blockchains that can
address [a variety of needs](https://substrate.io/ecosystem/projects/).

Review the [FRAME runtime implementation](./runtime/src/lib.rs) included in this
template and note the following:

- This file configures several pallets to include in the runtime. Each pallet
  configuration is defined by a code block that begins with `impl
$PALLET_NAME::Config for Runtime`.
- The pallets are composed into a single runtime by way of the
  [`construct_runtime!`](https://paritytech.github.io/substrate/master/frame_support/macro.construct_runtime.html)
  macro, which is part of the [core FRAME pallet
  library](https://docs.substrate.io/reference/frame-pallets/#system-pallets).

### Pallets

The runtime in this project is constructed using many FRAME pallets that ship
with [the Substrate
repository](https://github.com/paritytech/polkadot-sdk/tree/master/substrate/frame) and a
template pallet that is [defined in the
`pallets`](./pallets/template/src/lib.rs) directory.

A FRAME pallet is comprised of a number of blockchain primitives, including:

- Storage: FRAME defines a rich set of powerful [storage
  abstractions](https://docs.substrate.io/build/runtime-storage/) that makes it
  easy to use Substrate's efficient key-value database to manage the evolving
  state of a blockchain.
- Dispatchables: FRAME pallets define special types of functions that can be
  invoked (dispatched) from outside of the runtime in order to update its state.
- Events: Substrate uses
  [events](https://docs.substrate.io/build/events-and-errors/) to notify users
  of significant state changes.
- Errors: When a dispatchable fails, it returns an error.

Each pallet has its own `Config` trait which serves as a configuration interface
to generically define the types and parameters it depends on.

## Alternatives Installations

Instead of installing dependencies and building this source directly, consider
the following alternatives.

### Nix

Install [nix](https://nixos.org/) and
[nix-direnv](https://github.com/nix-community/nix-direnv) for a fully
plug-and-play experience for setting up the development environment. To get all
the correct dependencies, activate direnv `direnv allow`.

### Docker

Please follow the [Substrate Docker instructions
here](https://github.com/paritytech/polkadot-sdk/blob/master/substrate/docker/README.md) to
build the Docker container with the Substrate Node Template binary.

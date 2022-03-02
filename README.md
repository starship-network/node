# Starship Node

Starship is a Substrate-based octnetwork appchain. Starship is committed to providing easy-to-use blockchain infrastructure and creating a one-stop comprehensive infrastructure platform, which aims to reduce the threshold and cost for developers, while bringing them great returns.

The idea of project is provide a platform infra for customer. From there, stacking service, building web3, explore token information will be the main of project.

- Stacking: user can use our platform network to connect to their wallet and stacking. Safety & get the profit.

- Building Web 3.0: If web 2.0 needs platform hosting system, web 3.0 will need the network platform. We will provide the solution for client which purpose fast and easy to use.

- Explore information: We will provide dashboard monitoring status network for client.

## Getting Started

Follow the steps below to get started with the Node Template, or get it up and running right from your browser
in just a few clicks using [Playground](https://playground.substrate.dev/) :hammer_and_wrench:

### Using Nix

Install [nix](https://nixos.org/) and optionally [direnv](https://github.com/direnv/direnv) and [lorri](https://github.com/target/lorri) for a fully plug
and play experience for setting up the development environment. To get all the correct dependencies activate direnv `direnv allow` and lorri `lorri shell`.

### Rust Setup

First, complete the [basic Rust setup instructions](./docs/rust-setup.md).

### Run

Use Rust's native `cargo` command to build and launch the template node:

```sh
cargo run --release -- --dev --tmp

// cargo +nightly run --release --features=runtime-benchmarks
```

### Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
```

## Run

The provided `cargo run` command will launch a temporary node and its state will be discarded after
you terminate the process. After the project has been built, there are other ways to launch the
node.

### Single-Node Development Chain

This command will start the single-node development chain with persistent state:

```bash
./target/release/starship-node --dev
```

Purge the development chain's state:

```bash
./target/release/starship-node purge-chain --dev
```

Start the development chain with detailed logging:

```bash
RUST_LOG=debug RUST_BACKTRACE=1 ./target/release/starship-node -lruntime=debug --dev
```

### Connect with Polkadot-JS Apps Front-end

Once the node template is running locally, you can connect it with **Polkadot-JS Apps** front-end
to interact with your chain. [Click here](https://polkadot.js.org/apps/#/explorer?rpc=ws://localhost:9944) connecting the Apps to your local node template.


### Note

Build customSpecRaw: 

```
./target/release/starship-node build-spec --disable-default-bootnode --chain quark > customSpec.json

```

```
./target/release/starship-node build-spec --chain=customSpec.json --raw --disable-default-bootnode > customSpecRaw.json
```


[![Open in Gitpod](https://img.shields.io/badge/Open_in-Gitpod-white?logo=gitpod)]( https://github.com/Vara-Lab/Sails-Factory-Contract-Template.git)


# Sails Factory Contract Template

# Deploy the Contract on the IDEA Platform and Interact with Your Contract

## Step 1: Open Contract on Gitpod

<p align="center">
  <a href="https://gitpod.io/#https://github.com/Vara-Lab/Sails-Factory-Contract-Template.git" target="_blank">
    <img src="https://gitpod.io/button/open-in-gitpod.svg" width="240" alt="Gitpod">
  </a>
</p>

## Step 2: Configure gitpod to compile the contract

- Rust: You need to have rust 1.81 or newer to be able to compile your contract: 

```bash
rustup install 1.81
rustup default 1.81
rustup target add wasm32-unknown-unknown
```

- Next, you need to install the wasm-opt (to optimize WebAssembly files):

```bash
sudo apt install binaryen
```

## Step 3: Compile and Deploy the Smart Contract

### Compile the smart contract by running the following command:

```bash
cargo build --release
```

Once the compilation is complete, locate the `wasm.opt.wasm` file in the `target/wasm32-unknown-unknown/release` directory.

## Step 4: Interact with Your Contract on Vara Network

1. Access [Gear IDE](https://idea.gear-tech.io/programs?node=wss%3A%2F%2Frpc.vara.network) using your web browser.
2. Connect your Substrate wallet to Gear IDE.
3. Upload the `wasm.opt.wasm` and `app.idl` files by clicking the "Upload Program" button.
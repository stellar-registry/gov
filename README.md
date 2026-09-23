# stellar-registry/gov

Mainnet governance requests for [Stellar Registry](https://stellar.rgstry.xyz).

## Why this repo, and why mainnet is different from testnet

Root-registry changes (adding a Wasm or contract, creating a subregistry)
are gated behind a `manager` account on the registry contract. On
**testnet**, that manager is a Tansu-DAO-gated contract
(`registry-tansu-manager`), so those changes go through an on-chain
[Tansu](https://testnet.tansu.dev/governance/?name=stellarregistry) proposal,
vote, and execution — see the [rgstry.xyz governance
forms](https://stellar.rgstry.xyz/governance).

**Mainnet's manager is still a plain admin key** — there's no on-chain DAO
gating there _yet_. So on mainnet, a request starts here as a GitHub issue
instead: a maintainer reviews it and runs the requested change by hand.

Opening an issue against a template pre-fills the transaction a maintainer
needs to run — see [#1](https://github.com/stellar-registry/gov/issues/1)
for a real (pre-template) example of how one of these played out.

## Templates

| Template | Covers |
| --- | --- |
| [Add contract to root registry](.github/ISSUE_TEMPLATE/add-contract-to-root-registry.yml) | Register an already-deployed contract instance in the root registry |
| [Create a new subregistry](.github/ISSUE_TEMPLATE/create-a-new-subregistry.yml) | Deploy a new named channel in the root registry |

To add wasm to root registry, or for any other governance request, [open a blank issue](https://github.com/stellar-registry/gov/issues/new).

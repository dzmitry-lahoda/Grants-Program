# cw-xcm-executor

> This document will be part of the terms and conditions of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines (except for the title)! Lines starting with a `>` (such as this one) should be removed. Please use markdown instead of HTML (e.g. `![](image.png)` instead of `<img>`). 
>
> See the [Grants Program Process](https://github.com/w3f/Grants-Program/#pencil-process) on how to submit a proposal.
- **Team Name:** lahoda.pro
- **Payment Address:** TODO! BTC, Ethereum (USDT/USDC/DAI) or Polkadot/Kusama (aUSD) payment address. Please also specify the currency. (e.g. 0x8920... (DAI))
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 1

## Project Overview :page_facing_up:

This is new application grand to provide Substrate `xcm-executor` pallet compatible pallet as IBC enabled CosmWasm executor contract. 

### Overview

Project is about porting XCM executor to other Rust WASM contracts ecosysgem in Cosmos eocystem.

`cw` stands for CosmWasm and is standard prefix for contracts in Cosmos ecosystem.

`IBC` stands for Inter Blockchain Communication and is standard for trustless chains agnosics ledgers messages exchange. 

`xcm-executor` will be base to execute messages send from Kusama to Cosmos based chains and executor. 

So it will be making XCM message originated on any Dotsama IBC chain to run on any IBC CW Cosmos chain.

We believe that XCM is viable future of cross chain contracts and naturally fits IBC CW event and will allow brinig more utility into both ecosystems.


### Project Details


Output of this project would be:
- Contract running in CW test enviroment executing tests
- Porting `xcm-executor` pallet tests agains this contract
- ICS specification of contract

Main entry point of CW contract is `execute` message which dispatches contract exeuction
```rust
TODO!: message
```

Contact will store:
```
- XCM message
- pointer to message which is executed
```

Contrat will be initilaied (instantiated)
```
Owner of contract
```

Owner will be IBC enabled contact.

Will use
```
cw-
cw-multitet
```

will depend on
```
scale-
xcm
```

XCM executor confuration depends on:

T1
T1 

will be handled as message

transaction palyoad would be expected  to be CW encocde contract address and message

will provide ICS specification of contract

We expect the teams to already have a solid idea about your project's expected final state. Therefore, we ask the teams to submit (where relevant):

- Mockups/designs of any UI components
- Data models / API specifications of the core functionality
- An overview of the technology stack to be used
- Documentation of core components, protocols, architecture, etc. to be deployed
- PoC/MVP or other relevant prior work or research on the topic


Will not provide:
- IBC integration enpoint. Expected that commercial entity using this conrract will have other contract or Cosmos module invoking XCM contract.
- CW is planned to be no_std enabled (cw is already, cw-storate-plus) is. So it is not expected that these crates witll be made no_std, so it is viable to do so.
- `Transact` message payload builder.
- Audit

### Ecosystem Fit

Project proves portability and cross chain viability of XCM format. Allows alternative executor on no_std cosmwasm VM running as pallet.

Target adiomce developers build on top or parachins integratin with Cowsmas/Cosmos/IBC system via XCM.

It enableer to allows to transfer tokens, oracle data and govenrnace for and to Dotsama easy way.

There are other projects expandin XCM to Etherem or bridges. So none I am aware of expanidn it to Cosmos.

## Team :busts_in_silhouette:

### Team members

- Dzmitry Lahoda

Scope is small enought to be handled by one person.

### Contact

- **Contact Name:** Dzmitry Lahoda
- **Contact Email:** dzmitry@lahoda.pro
- **Website:** lahoda.pro

### Team's experience

I am working with Composable Finance for enabling their XCVM message format executed over Cosmwasm and IBC. And at same time I did setu Composable runtimes to handle XCM message.

Before that I was wring smart contracts for Fluence(they have Aqua language for cross chain messaging) and Solana(contracts).

### Team Code Repos

- https://github.com/<your_organisation>/<project_1> <- just me conrib
- https://github.com/<your_organisation>/<project_2>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/<person_1> <- dz


## Development Status :open_book:

If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues, 
- pR to CW std for storage
- move from CW repo, limk to XCM compile

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. To assist you in defining it, we have created a document with examples for some grant categories [here](../docs/grant_guidelines_per_category.md). Since these will be part of the agreement, it helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your project is related to Substrate, Kusama or Polkadot. We _recommend_ that teams structure their roadmap as 1 milestone ≈ 1 month.

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Teams that submit others' work without attributing it will be immediately terminated.**

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). Note that the acceptance criteria and additional benefits vary depending on the [level](../README.md#level_slider-levels) of funding requested. This and the costs for each milestone need to be provided in USD; if the grant is paid out in Bitcoin, the amount will be calculated according to the exchange rate at the time of payment.

### Milestone 1 Example — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 8,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) |
| 2. | Substrate module: Y | The Y Substrate module will... |
| 3. | Substrate module: Z | The Z Substrate module will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


### Milestone 2 Example — Additional features

- **Estimated Duration:** 2 month
- **FTE:**  1,5
- **Costs:** 10,000 USD

...


## Future Plans

- apply for grand to IBC/CW enabled Cosmos chain to integrate XCM executor.

## Referral Program (optional) :moneybag: 

You can find more information about the program [here](../README.md#moneybag-referral-program).
- **Referrer:** Name of the Polkadot Ambassador or GitHub account of the Web3 Foundation grantee
- **Payment Address:** BTC, Ethereum (USDT/USDC/DAI) or Polkadot/Kusama (aUSD) payment address. Please also specify the currency. (e.g. 0x8920... (DAI))

## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** Web3 Foundation Website

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.

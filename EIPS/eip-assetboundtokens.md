---
title: <Non-Fungible Asset Bound Token>
description: <An interface for Non-Fungible Asset Bound Tokens, also known as a NFABT.>
author: <<Mihai Onila (@MihaiORO), Nick Zeman (@NickZCZ), Narcis Cotaie (@NarcisCRO)>
discussions-to: <URL>
status: Idea
type: <Standards Track, Meta, or Informational>
category: <ERC> # Only required for Standards Track. Otherwise, remove this field.
created: <date created on, in ISO 8601 (yyyy-mm-dd) format>
requires: <EIP number(s)> # Only required when you reference an EIP in the `Specification` section. Otherwise, remove this field.
---


<!--
  READ EIP-1 (https://eips.ethereum.org/EIPS/eip-1) BEFORE USING THIS TEMPLATE!

  This is the suggested template for new EIPs. After you have filled in the requisite fields, please delete these comments.

  Note that an EIP number will be assigned by an editor. When opening a pull request to submit your EIP, please use an abbreviated title in the filename, `eip-draft_title_abbrev.md`.

  The title should be 44 characters or less. It should not repeat the EIP number in title, irrespective of the category.

  TODO: Remove this comment before submitting 
-->

## Abstract

A standard interface for Non-Fungible Asset Bound Tokens (NFABT/s), a subset of the more general Asset Bound Token (KBT/s).

The following standard allows for the implementation of a standard API for tokens within smart contracts and removes basic functionality to the `transferFrom`and `approve` functions. In doing so, the ABT cannot be transferred in the traditional sense as it’s intended to be transferred with a specific asset. 

New read functions are referred to as ‘Linked’ functions such as ‘linkedTotalSupply’ and ‘linkedContract’. This information will point to the and reflect the information of the linked collection. 

We considered ABTs being used by every individual who wish to link an additional non-fungible asset to an already existing non-fungible asset. ABT’s allow tokens to be bound together, allowing them to symbiotically work together rather than causing separation despite being created at different times.


## Motivation

Currently only wallets or addresses can own an asset. With the rise of numerous digital collectables and the idea of digital identity, entities must create a second collection when the first one can no longer support the evolution of an idea, or rather it’s simply a new idea overall.
What we see happening time and time again, is the creation of a secondary smart contract, often a secondary collection, that does little for the first. If anything, a negative impact on the first can be recorded as the creator must split his attention in 2 with the creation of a secondary smart contract. Oftentimes this leads to holders of collection one selling their assets on the market, in an attempt to get a more sought after asset within collection 2. The result is liquidity being pulled from the 1st collection, and allocated into the second, rarely benefiting the first collection in any way.

In a different setting, we can observe the issuance of IDs happening in every nation, such as a passport. This document can be used to not only identify oneself, but also to link individuals to their healthcare insurance, driver license, bank accounts and so on. If we are to see the creation of a universal digital identification ID, the idea that each of these documents should not be linked or connected can result in major issues. For example, a smart contract is made for each of these, minting a token for each. If a user decides to switch wallets, they must pay close attention to send all of these tokens as to not get lost. The concept of an on-chain identity is not a farfetched idea, but requiring the individual to migrate all issued tokens from various identities can be catastrophic.

ABTs is a token standard that bind one token to another token by linking it. This means if the primary token gets moved, all of the linked tokens information will update, essentially moving with it without the act of the token actually moving. The token standard can be viewed as a live repository, updating in accordance with the primary token while remaining independent with its own set of information. Therefore, whether it’s a secondary collection intended to complement the first, or healthcare issued to an ID, the smart contract is complementary and does not compete with the first, but rather adds to it.


## Specification

<!--
  The Specification section should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (besu, erigon, ethereumjs, go-ethereum, nethermind, or others).

  It is recommended to follow RFC 2119 and RFC 8170. Do not remove the key word definitions if RFC 2119 and RFC 8170 are followed.

  TODO: Remove this comment before submitting
-->

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 and RFC 8174.

## Rationale

<!--
  The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages.

  The current placeholder is acceptable for a draft.

  TODO: Remove this comment before submitting
-->

TBD

## Backwards Compatibility

This standard is fully ERC-721 and ERC-6809 compatible.

## Test Cases

<!--
  This section is optional for non-Core EIPs.

  The Test Cases section should include expected input/output pairs, but may include a succinct set of executable tests. It should not include project build files. No new requirements may be introduced here (meaning an implementation following only the Specification section should pass all tests here.)
  If the test suite is too large to reasonably be included inline, then consider adding it as one or more files in `../assets/eip-####/`. External links will not be allowed

  TODO: Remove this comment before submitting
-->

## Reference Implementation

<!--
  This section is optional.

  The Reference Implementation section should include a minimal implementation that assists in understanding or implementing this specification. It should not include project build files. The reference implementation is not a replacement for the Specification section, and the proposal should still be understandable without it.
  If the reference implementation is too large to reasonably be included inline, then consider adding it as one or more files in `../assets/eip-####/`. External links will not be allowed.

  TODO: Remove this comment before submitting
-->

## Security Considerations

Asset Bound Tokens are linked to another non-fungible token. If an individual loses access to this mother token, they also losses access to all ABT tied to it. This is why we strongly recommend utilizing a ERC-6809 as the mother token, as Non-Fungible Key Bound Tokens were designed with security in mind every step of the way and way to retrieve the token incase access to the wallet is lost or connected to a malicious site. 

Needs discussion.

## Copyright

Copyright and related rights waived via [CC0](../LICENSE.md).

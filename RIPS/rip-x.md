---
rip: x
title: Precompile for secp256r1 Curve Support
description: Proposal to add `P256VERIFY` precompiled contract to the rollups due to the EIP-7212 specifications.
author: Ulaş Erdoğan (@ulerdogan), Doğan Alpaslan (@doganalpaslan)
discussions-to: https://ethereum-magicians.org/t/eip-7212-precompiled-for-secp256r1-curve-support/14789
status: Last Call
type: Standards Track
category: Core
created: 2023-11-21
---

## Abstract

This RIP proposes that the [EIP-7212](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7212.md), which creates a precompiled contract that performs signature verifications in the “secp256r1” elliptic curve, be standardized for rollups and integrated into multiple chains independently of the Ethereum protocol by following the original EIP specifications.

## Motivation

The rollups have a more flexible ecosystem than the L1 to implement new features and protocol changes. The EIP-7212 comes forward as a good candidate to obtain adoption with several use-cases in the L2 ecosystem, then be implemented into the L1 as a proven and battle-tested modification.

## Specification

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 and RFC 8174.

The specifications MUST follow the [EIP-7212](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7212.md#specification) which defines the interface, precompiled contract operation, and gas cost.

## Rationale

As discussed in the RollCall#0, RIPs has a significant role to coordinate EVM-like L2s to create improvement standards. Most of the rollups noticed their willingness to implement the [EIP-7212](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7212.md). Accordingly, this RIP is created to standardize the EIP implementations for the rollups.

## Backwards Compatibility

No backward compatibility issues found as the precompiled contract will be added to the next available address in the precompiled address set.

## Test Cases

Several test cases have been defined in the original proposal, [EIP-7212](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7212.md#test-cases).

## Reference Implementation

Implementation of the `P256VERIFY` precompiled contract is applied to go-ethereum client to create a reference. This implementation can be followed by the rollup client teams to integrate the precompiled contract.

## Security Considerations

There is a risk might be occured from miscommunications between the L1 and rollup protocols, such as having a different implementations in different protocols. The proposal should be discussed between RIP working group and get advised from the L1 development teams to foresee future inconsistencies.

## Copyright

Copyright and related rights waived via [CC0](../LICENSE.md) which is defined in the original proposal, [EIP-7212](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7212.md#copyright).
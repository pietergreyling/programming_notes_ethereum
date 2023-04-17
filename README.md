# Ethereum Programming Notes
These notes help to aid my short term memory.

### The Ethereum Virtual Machine (EVM) Architecture

![EVM Architecture Overview](./images/evm.png)

#### The EVM Stack / Instructions / Gas

- https://ethereum.org/en/developers/docs/evm/#evm-instructions

The EVM executes as a stack machine(opens in a new tab)↗ with a depth of 1024 items. Each item is a 256-bit word, which was chosen for the ease of use with 256-bit cryptography (such as Keccak-256 hashes or secp256k1 signatures).

During execution, the EVM maintains a transient memory (as a word-addressed byte array), which does not persist between transactions.

Contracts, however, do contain a Merkle Patricia storage trie (as a word-addressable word array), associated with the account in question and part of the global state.

Compiled smart contract bytecode executes as a number of EVM opcodes, which perform standard stack operations like XOR, AND, ADD, SUB, etc. The EVM also implements a number of blockchain-specific stack operations, such as ADDRESS, BALANCE, BLOCKHASH, etc.

![EVM Stack / Instructions / Gas](./images/gas.png)

## Resources

### The Ethereum Virtual Machine

#### ETHEREUM VIRTUAL MACHINE (EVM)

- https://ethereum.org/en/developers/docs/evm/

The EVM’s physical instantiation can’t be described in the same way that one might point to a cloud or an ocean wave, but it does exist as one single entity maintained by thousands of connected computers running an Ethereum client.

The Ethereum protocol itself exists solely for the purpose of keeping the continuous, uninterrupted, and immutable operation of this special state machine. It's the environment in which all Ethereum accounts and smart contracts live. At any given block in the chain, Ethereum has one and only one 'canonical' state, and the EVM is what defines the rules for computing a new valid state from block to block.

#### OPCODES FOR THE EVM

- https://ethereum.org/en/developers/docs/evm/opcodes/

#### An Ethereum Virtual Machine Opcodes Interactive Reference

- https://www.evm.codes/?fork=shanghai

#### The Ethereum Blockchain Explorer

- https://etherscan.io/

#### What is an Ethereum Virtual Machine (EVM) and how does it work?

- https://cointelegraph.com/news/what-is-an-ethereum-virtual-machine-evm-and-how-does-it-work




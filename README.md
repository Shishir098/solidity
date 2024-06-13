# MyToken Smart Contract

This is a simple ERC20-like token contract implemented in Solidity. The contract allows minting and burning of tokens, with public variables to store token details and a mapping to manage balances.

## Requirements

1. The contract contains public variables that store the details about the token:
    - Token Name
    - Token Abbreviation
    - Total Supply

2. The contract has a mapping of addresses to balances: `mapping(address => uint)`.

3. There is a `mint` function that takes two parameters: an address and a value. The function increases the total supply by the given value and increases the balance of the specified address by that amount.

4. There is a `burn` function that works oppositely to the mint function. It takes an address and a value, deducts the value from the total supply, and decreases the balance of the specified address by that amount.

5. The `burn` function includes conditionals to ensure that the balance of the specified address is greater than or equal to the amount to be burned.

## Contract Details

### Public Variables

- `string public tokenName = "GMECoin";`
  - The name of the token.
  
- `string public tokenAbbrv = "GME";`
  - The abbreviation of the token.
  
- `uint public totalSupply = 0;`
  - The total supply of the token, initialized to 0.

### Mapping

- `mapping(address => uint) public balances;`
  - A mapping to store the balances of addresses.

### Functions

- `function mint(address _address, uint _value) public`
  - Increases the total supply by `_value`.
  - Increases the balance of `_address` by `_value`.

- `function burn(address _address, uint _value) public`
  - Checks if the balance of `_address` is greater than or equal to `_value`.
  - If true, decreases the total supply by `_value`.
  - Decreases the balance of `_address` by `_value`.

## Usage

To use this contract, you can deploy it to an Ethereum-compatible blockchain and interact with it using web3 libraries or Ethereum clients.

### Example

```solidity
// Deploy the contract
MyToken myToken = new MyToken();

// Mint tokens
myToken.mint(0xYourAddress, 100);

// Burn tokens
myToken.burn(0xYourAddress, 50);
SPDX-License-Identifier
This contract uses the MIT license.

solidity

// SPDX-License-Identifier: MIT
Pragma
This contract is written for Solidity version 0.8.18.
solidity

Author
Github:-https://github.com/Shishir098
Email:-shishirgautam12345@gmail.com

pragma solidity ^0.8.18;
License
This project is licensed under the MIT License.









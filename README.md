# Create a Token

This solidity program provides the basic knowledge for to those who are starting to create their own token. The purpose of this program is to serve as a starting point for those who are new to making their own tokens

## Description

This program is written in solidity a programming language used for developing smart contracts on the Ethereum blockchain. This contract has three variables to name the token , to give abbreviation to your token , and get total supply. Next it has two simple funtions one for minting and other for burning token

## Getting Started

### Installing

* You can access this program through my github repository link 
* NO modifications needed to access files/Folders

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
* Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. 
* Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
 // SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

     string public tokenName = "Survivor";
     string public tokenAbbrev="SVR";
     uint public totalSupply=0;

     mapping(address => uint) public balances;

     function mint(address _address,uint _value) public {
      totalSupply+= _value;
      balances[_address] += _value;
     }
    function burn (address _address,uint _value) public {   
      if(balances[_address]>= _value){
      totalSupply -= _value;
      balances[_address] -= _value;
     }
}
}
```

## Author
Shubham Dubey




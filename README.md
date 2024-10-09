# Solidity Assesment
Project that has a mint and burn token function

Description
Metacrafters solidity assesment - ETH PROOF: Beginner EVM Course

Getting Started
1. Open https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.26+commit.8a97fa7a.js
2. Create a solidity file with .sol as its filename
3. Copy and paste the code below

// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyNewToken {

    // public variables here
    string public tokenName = "LuwisMigel";
    string public tokenAbbrv = "LM";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }

}

4. Compile and run the project

5.Deploy the project

Note: If 0.8.26 version is having issues for you, try using other versions.

Author
Luis Miguel C. Dela Cruz
202110441@fit.edu.ph

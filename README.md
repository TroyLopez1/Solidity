# Create a Token

As we are using a Solidity programming language this project aims to create a simple token that holds value. 
This project is will build and deploy unique digital currency on the ethereum blockchain


## Description

This is a step by step program that in creating own custom token on the ethereum blockchain using solidity.
In this project will includes its syntax, data types, functions, and control strutures foe smart contact deployment


## Getting Started

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

### Executing program

When in remix start the Project by clicking the New File under that Files section and enter the name of the project and hit enter.
Paste the provided code to the remix
```
contract MyToken {

    // public variables here
    string public tokenName = "Troy";
    string public tokenAbbrv = "LPZ";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
    }
}
}

```
After putting the code in the remix , In compiling there is a "Solidity Complier" Tab and in "Advance Configurations" click the "Compile (Name of the file)" option above the "Compile and Run Script"
After compiling go to "Deploy and Run Transactions" click deploy and it will provide the Deployed Contracts. 
After Deploying copy the address in the account and paste it on Mint under Deployed Contracts under adress put the desire value 
and hit transact , Check if it runs it will provide a value in totalSupply by clicking it will display the value same goes in balances just provide the same address in the blank space. 
to check if burning value is working just paste again the adreess and put the desire value that want to burn in the value if mint.


## Authors

Contributors names and contact info

Lopez, Julian Caster Troy 


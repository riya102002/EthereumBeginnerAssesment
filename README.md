
# MyToken using Solidity

This Solidity programme serves as an example of fundamental Solidity programming language ideas. It is a straightforward token contract. The objective of this program is to give a starting point for people who are new to Solidity and wish to understand the generation and manipulation of tokens on the Ethereum network.




## Description
This programme defines a Solidity smart contract that carries out a simple token system. The name, abbreviation, and total supply of the token are stored as public variables included in the contract. Additionally, it has a mapping to monitor balances for several addresses. The contract also includes functions that demonstrate basic token activities, such as minting (creating) and burning (destroying) tokens.

## Getting Started
Execution :

You may use the online Solidity IDE Remix to execute this programme. Visit the Remix website at Remix Ethereum to get started.

Click the "+" symbol in the left-hand sidebar to start a new file once you are on the Remix website. Save the file (MyToken.sol, for example) with the.sol extension. The code below should be copied and pasted into the file:
stability. Copy the below code:


 //SPDX-License-Identifier: MIT


pragma solidity 0.8.18;

contract MyToken 

{

    // public variables here
    
    string public T_name='Tista';
    
    string public T_abbrv='Tis';
    
    uint public Total_supply=0;

    // mapping variable here
    mapping(address => uint)public balances;

    // mint function
    function minting(address add,uint value)public
    {
          Total_supply=Total_supply + value;
          balances[add]+=value;
    }

    // burn function
    function burn_token(address add,uint value)public
    {
        if(balances[add]>=value)
        {
         Total_supply-= value;
          balances[add]-=value;   
        }
    }
}


Select the "Solidity Compiler" tab from the sidebar on the left to begin compiling the code. Click "Compile MyToken.sol" after ensuring that the "Compiler" option is set to "0.8.18" (or another suitable version).

Selecting the "Deploy & Run Transactions" tab from the left-hand sidebar will allow you to deploy the contract after the code has been built. Click the "Deploy" button after choosing the "MyToken" contract from the dropdown menu.

You may communicate with the contract by invoking the burn_token and minting methods to control the token supply once it has been deployed. By using the corresponding public variables, you may verify balances and total supplies.


## Author

 @RiyaKesharwani [https://github.com/riya102002]



## License

[MIT](https://choosealicense.com/licenses/mit/)

This project MyToken is licensed under the MIT license


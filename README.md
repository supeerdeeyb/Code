Project: Create a Token 
This Solidity program is a simple Creating a token program that demonstrates the basic syntax and functionality of the Solidity programming language. 
This will demonstrate how the token works 

Description
This program using basic syntax function for beginners that uses data types and mapping
This will help you gain more knowlege about the Programming langauge 

Executing Program 
To execute this program you need to use online IDE of Solidity 
E.g. https://remix.ethereum.org/ 
Once you open the link, you will create a file on the contract folder and the file name 
should be ending with ".sol" 

contract MyToken {

    // public variables here
   string public tokenName = "Dave";
   string public tokenAbbrv = "DVE";
   uint public totalSupply = 0; 

    // mapping variable here
   mapping (address => uint) public balances;

    // mint function
   function mint (address _address, uint _value) public {
    totalSupply += _value;
    balances [_address] += _value;
   }

    // burn function
   function burn (address _address, uint _value) public {
    if (balances [_address] >= _value) {
    totalSupply -= _value;
    balances [_address] -= _value;
   }
   }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed you can interact with the code using transact button 

Author
John Dave Rizada
422002188@ntc.edu.ph

# ETH-PROOF-Beginner-Assignment
This is my ETH-PROOF-Beginner-Assignment where I have created a token to Mint and Burn coins.

<h1>Description</h1>
This program is a simple token contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract stores details about a custom token, including its name, abbreviation, and total supply. It also maintains a mapping of addresses to balances, allowing for the tracking of token ownership. The contract includes mint and burn functions to manage the supply of tokens, making it a straightforward introduction to token creation and management in Solidity.

<h1>Getting Started</h1>
<h2>Executing program</h2>
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Assessment.sol). Copy and paste the following code into the file:

    contract MyToken {
    // public variables here
    string public tokenName= "Saket";
    string public tokenAbbrv= "SA";
    uint public totalSupply= 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply+= _value;
        balances[_address]+= _value;
    }
    // burn function
    function burn(address _address, uint _value) public {
        if(balances[_address] >=_value){
            totalSupply-= _value;
            balances[_address]-= _value;
        }
    }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Assessment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Assessment" contract from the dropdown menu, and then click on the "Deploy" button.

To mint new tokens, use the mint function by providing an address and the amount of tokens to mint.
To burn tokens, use the burn function by providing an address and the amount of tokens to burn. The function checks if the balance is sufficient before burning.
<h2>Authors</h2>
Saket Agarwal

<h2>License</h2>
This project is licensed under the MIT License - see the LICENSE.md file for details

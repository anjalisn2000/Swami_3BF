# Swami_3BF
Functions
[I] Functions
CODE:
// SPDX-License-Identifier: MIT 
pragma solidity >=0.4.22 <0.9.0;

contract Test {
    function return_example() 
        public
        pure
        returns (
            uint256, 
            uint256, 
            uint256,
            string memory
        )
    {
        uint256 num1 = 10; 
        uint256 num2 = 16;
        uint256 sum = num1 + num2; 
        uint256 prod = num1 * num2; 
        uint256 diff = num2 - num1;
        string memory message = "Multiple return values"; return (sum, prod, diff, message);
    }
}
====
 [II] Function Modifiers
CODE:
// SPDX-License-Identifier: MIT 
pragma solidity >0.5.0;

contract ExampleContract {
    address public owner = 0x5B38Da6a701c568545dCfcB03FcB875f56beddC4; 
    uint256 public counter;

    modifier onlyowner() {
        require(msg.sender == owner, "Only the contract owner can call");
        _;
    }

    function incrementcounter() public onlyowner { 
        counter++;
    }
}
===================================================
 [III] View Functions
pragma solidity >0.5.0;
contract view_demo { 
    uint256 num1 = 2; 
    uint256 num2 = 4;

    function getResult() public view returns (uint256 product, uint256 sum) { 
        product = num1 * num2;
        sum = num1 + num2;
    }
}
=================================================
IV] Pure Function
pragma solidity >0.5.0;

contract pure_demo {
    function getResult() public pure returns (uint256 product, uint256 sum) { 
        uint256 num1 = 2;
        uint256 num2 = 4;
        product = num1 * num2; sum = num1 + num2;
    }
}
===============================
 V] Mathematical Functions
CODE:
pragma solidity >0.5.0; 
contract Test{
    function CallAddMod() public pure returns(uint){ 
        return addmod(7,3,3);
    }

    function CallMulMod() public pure returns(uint){ 
        return mulmod(7,3,3);
    }
}
============================
 VI] Cryptographic Functions

CODE:
pragma solidity >0.5.0; 
contract Test{
    function callKeccak256() public pure returns(bytes32 result){ 
        return keccak256("BLOCKCHAIN");
    }

    function callsha256() public pure returns(bytes32 result){ 
        return sha256("BLOCKCHAIN");
    }

    function callripemd() public pure returns (bytes20 result){ 
        return ripemd160("BLOCKCHAIN");
    }
}
=======================================
VII] Function Overloading[7,8  add--Welcome]

// SPDX-License-Identifier: MIT 
pragma solidity ^0.8.0;

contract OverloadingExample {
    function add(uint256 a, uint256 b) public pure returns (uint256) { 
        return a + b;
    }

    function add(string memory a, string memory b) 
        public
        pure
        returns (string memory)
    {
        return string(abi.encodePacked(a, b));
    }
}
=============================

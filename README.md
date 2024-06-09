# smart contract project 
We created a contract to handle different statements in solidity example (require(),assert(),revert())

## Description

This is project created to demonstrate the usage of require(),assert(),revert() statement .
In this we create function which takes age of father and son and revert according to the conditon .

## Getting Started

### Installing

* to deploy this code you need to have remix or any IDE.
* need compiler for solidity 
* required version of solidity compiler is (version ^0.8.0)

### Executing program

*to deploy this block of code you need an IDE of  solidity
* after that copy paste the given block of code in your IDE
* then set compiler to version (0.8.0)
* then deploy the assertsol contract
* then implement the summation function
* the require()statement ensures that father age should not be zero
* the assert() statement ensures that the father age shoul be greater than son's age 
* the revert()statement check the difference of father and son age and if the differnce is less than 10 revert with and error mesage .



// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.0;

contract Assertsol {
    function summation(uint256 father_age, uint256 son_age) external pure returns (uint256) {
        // require statement
        require(father_age != 0, "father_age cannot be zero.");

        // assert statement
        assert(father_age >= son_age);

        // Perform the difference 
        uint256 difference_age = father_age - son_age;

        // revert statement
        if (difference_age <10) {
            revert("father is not so much elder than son ");
        }

        return difference_age;
    }
}

## Help
* make sure your IDE is for solidity 
*  make sure your compiler is set to version (0.8.0) otherwise error will throw

## Authors

kumar sanjeev 
https://www.linkedin.com/in/kumar-sanjeev-150965230/


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

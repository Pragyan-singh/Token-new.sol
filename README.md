# Project Title

New Token Creation and Applying Changes in it

## Description

In this code we are going to create a new token named Gyan and abbrivation "Gyn" in contract together.

```
string public tokenname="Gyan";
string public tokenabbr="Gyn";
uint public totalsupply=0;
```

Firstly Declaring TokenName, Tokenabbr, and Totalsupply.

```
mapping(address=>uint) public balance;
```

Then mapping address of account to the balance.

```
function mint(address _adrs, uint _value) public {
        totalsupply += _value;
        balance[_adrs]+=_value;
    }
```

Declaring and defining mint function to add values to the balance in account.

```
function burn(address _adrs, uint _value) public returns(bool) {
        if(balance[_adrs]>=_value){
            totalsupply -= _value;
            balance[_adrs] -= _value;
            return false;
        }
        return true;
        
    }
```

Declaring and defining burn function to deduct values from balance.
using if statement to check the condition that balance should not be less than deducting value.


## Getting Started

### Installing

* Run this Program on Remix.
* No modification needed

### Executing program

* After pasting this code on remix, hit the compile button on solidity compiler on left hand side bar.
* After compiling, then go on compile and run tab on left hand side bar.
* Deploy the Program.
* Go on Deployed Contracts, in mytoken use following function,
* use burn function to deduct value from my balance.
* use mint function to add value to balance.
* use total supply to check value in balance.


// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract EtherUnitConverter {
    address public etherOwner = msg.sender;
    
    mapping (address => uint )balance;
    

    event etherReceived (address indexed sender , uint etherAmount);

    function receiveEther(uint amount) external payable {
        balance[etherOwner]+=amount;
        
        emit etherReceived(msg.sender, msg.value);
        
    }

    function etherAmountReceived() public view returns(uint) {
        return balance[msg.sender];
    }
    

    function etherToWei() public view returns(uint) {
        return balance[etherOwner] * 1 ether;
    }

    function etherToGwei() public view returns(uint) {
        return balance[etherOwner] * 1 gwei;
    }
    
    
}

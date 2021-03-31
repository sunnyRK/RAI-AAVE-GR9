# RAI X Aave Challenge (Gitcoin GR9)

## Challenge

For this challenge, you’re invited to build an insurance solution where Safe owners can deposit ETH on Aave and keep the received aETH in a saviour contract. When a Safe gets liquidated, the saviour should redeem ETH from Aave and add it in the Safe.

## Solution

I have used code of the Refelexr geb-safe-saviours.
you can check my code submission in [src/saviours/AaveSafeSaviour.sol](https://github.com/sunnyRK/RAI-AAVE-GR9/blob/master/src/saviours/AaveSafeSaviour.sol).

I have create a AAVE Safe Saviour contract. Where user can deposit ETH on AAVE and keep recieved aETH on sviuor contract. which will be Safe to gets liquidited.

[Here you can see AaveSafeSaviour Implementation.](https://github.com/sunnyRK/RAI-AAVE-GR9/blob/master/src/saviours/AaveSafeSaviour.sol)

## Implementation Methods

`deposit: ` where user come with its safeID and ETH. deposit eth into aave and get aETH and keeps it in Saviour Contract.

`witdraw: ` Where user come with its safeID and colleteral token amount. and function transfer aETH into ETH and tranfer to user as per collateral token amout.

`saveSAFE: ` It will be called by liquidation engine. If somepoint your collateral position down then liquidation engine will call saveSafe method and takes ETH from saviour contract and add into SAFE contract to save your position.

## Kovan Deployed Contract Address

For AAVE Saviour
https://kovan.etherscan.io/address/0x8774c700d008157d840f391cb80b5bb80a759b81#code
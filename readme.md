# SAVE GAS
- The gas itself is calculated according to the operations we do that have a certain cost per operation (Gas)
- Gas Price is what the network is willing to accept in terms of gas price in order to do the operations that we spoke before, which is something variable
- This system serves to compensate those that help the network
Gas Fee = Gas Price * Gas
## What should be consider when trying to save gas
- We should avoid accessing the same data multiple times if that data is constant
  ex:
  ```
  uint[] public test
  t = test[x]
  y = t + 2
  k = test[x] + 2

  instead of

  uint[] public test
  y = test[x] + 2
  k = test[x] * 2
  ```
- Avoiding saving data that you can easily put in events. You cannot access it inside of the smart contract so be carefull with that in case your logic depends on it
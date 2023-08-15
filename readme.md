The "QMFToken" contract is a smart contract that inherits from the ERC20 standard token contract and includes additional features like transaction fees and token burning.

**Constructor Initialization:**
The constructor of the "QMFToken" contract is invoked. It initializes the token by setting its name to "Quamfy" and its symbol to "QMF". Additionally, an initial supply of 100,000,000 QMF tokens is minted and assigned to the address that deployed the contract (referred to as "msg.sender"). The constructor also sets a burn threshold of 50,000,000 QMF tokens and a fixed fee amount of 0.001 QMF tokens (1 * 10^15) for transactions.

**Additional Getter and Setter Functions:**
The contract provides external getter functions to retrieve specific information:

* `getFee()`: Returns the current transaction fee amount.
* `getBurnThreshold()`: Returns the current burn threshold value.
* `getMasterWallet()`: Returns the address of the master wallet designated to receive transaction fees.

In addition to getter functions, the contract includes setter functions that can be accessed by the owner of the contract:

* `setBurnThreshold(uint256 _burnThreshold)`: Allows the owner to update the burn threshold value. This is useful for adjusting when token burning should occur based on changing conditions.
* `setFeeAmount(uint256 _feeAmount)`: Permits the owner to modify the transaction fee amount. This can help adapt to varying transaction cost requirements.
* `setMasterWallet(address _masterWallet)`: Enables the owner to change the address of the master wallet responsible for receiving transaction fees.


# Coinbase Transaction

All transactions on the bitcoin network are not created equally. A coinbase transaction is a unique type of bitcoin transaction that can only be created by a miner. This type of transaction has no inputs, and there is one created with each new block that is mined on the network. In other words, this is the transaction that rewards a miner with the block reward for their work. Any transaction fees collected by the miner are also sent in this transaction. [Credit](https://blog.cex.io/bitcoin-dictionary/coinbase-transaction-12088)

### Test Driven Examples


```python
from io import BytesIO
from tx import Tx
from helper import little_endian_to_int

class Tx(Tx):
    
    def is_coinbase(self):
        '''Returns whether this transaction is a coinbase transaction or not'''
        # check that there is exactly 1 input
        # grab the first input
        # check that first input prev_tx is b'\x00' * 32 bytes
        # check that first input prev_index is 0xffffffff
        pass

    def coinbase_height(self):
        '''Returns the height of the block this coinbase transaction is in
        Returns None if this transaction is not a coinbase transaction
        '''
        # if this is NOT a coinbase transaction, return None
        # grab the first input
        # grab the first element of the script_sig (.script_sig.elements[0])
        # convert the first element from little endian to int
        pass
```

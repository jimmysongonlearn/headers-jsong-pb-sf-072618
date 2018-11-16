
# Block Headers

## Test Driven Examples


```python
# Exercise 3.1

from io import BytesIO
from network import GetHeadersMessage
from helper import (
    encode_varint,
    int_to_little_endian,
    little_endian_to_int
)

class GetHeadersMessage(GetHeadersMessage):

    def serialize(self):
        '''Serialize this message to send over the network'''
        # protocol version is 4 bytes little-endian
        # number of hashes is a varint
        # start block is in little-endian
        # end block is also in little-endian
        pass
```


```python
# Exercise 3.2

from io import BytesIO
from network import HeadersMessage
from helper import read_varint
from block import Block

class HeadersMessage(HeadersMessage):

    @classmethod
    def parse(cls, stream):
        # number of headers is in a varint
        # initialize the blocks array
        # loop through number of headers times
            # add a block to the blocks array by parsing the stream
            # read the next varint (num_txs)
            # num_txs should be 0 or raise a RuntimeError
        # return a class instance
        pass
```

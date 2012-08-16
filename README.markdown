# lazy-stream

A library for lazy evaluation in Node.js, with support for infinite sequences.

## Creating a stream

    stream = require 'stream'

    stream.range 9                       # naturals from 9 to infinity
    stream.create (-> 2), ((i) -> i*2)    # all powers of 2


## Stream operations

    myStream.filter (i) -> i%2 == 0       # a new stream with even numbers only
    myStream.take(5)                      # get the first 5 elements (javascript array)


## Try the sample code

    # in the project folder
    
    >  npm install
    >  npm install -g mocha
    >  mocha
    
    # all the tests should pass
    
    > coffee src/main.coffee

    # lots of prime numbers!

## See the unit tests for more examples...
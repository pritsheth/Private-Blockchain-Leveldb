# Private-Blockchain-Leveldb


The levelSandbox.js File

levelSandbox.js implements the data interaction for your Private Blockchain. It is the Data Access Layer for the application.

For this project, we will need to configure our private blockchain to persist data using LevelDB as the data access layer.

Review the documentation below as it will be very helpful when you need to implement functions to access data or to add data to the storage.

LevelDB Documentation - a light-weight, single-purpose library for persistence with bindings to many platforms.

In the file, we added the project dependencies, established the storage location for dataset, and configured the db object to reference level with chainDB as the location of our dataset.


Functionality
This file already has a few basic functions implemented for you:

- addLevelDBData(key,value)
- addDataToLevelDB(value)
- getLevelDBData(key)


# The simpleChain.js file
Purpose
simpleChain.js implements the classes that are part of your private blockchain application.

```
Block class
class Block{
    constructor(data){
     this.hash = "",
     this.height = 0,
     this.body = data,
     this.time = 0,
     this.previousBlockHash = ""
    }
}
```

The Block class contains all the attributes of a block. Review these elements and make sure you understand why each one is important in your Private Blockchain application.
```
Blockchain class
class Blockchain{
  constructor(){
    this.chain = [];
    this.addBlock(new Block("First block in the chain - Genesis block"));
  }
 ```
...
The Blockchain class currently implements all these functionalities in your application and all data is held within the chain array. In the next step, we will discuss how to modify these to persist data.

- addBlock(newBlock) - Adds a new block into the chain, to do that you need to assign the corresponding height, hash, previousBlockHash and timeStamp to your block.
- getBlockHeight() - Counts all the Blocks in your chain and give you as a result the last height in your chain
- getBlock(blockHeight) - Gets a block and returns it as JSON string object
- validateBlock(blockHeight) - Validates block data integrity
- validateChain() - Validates blockchain is still valid at any moment

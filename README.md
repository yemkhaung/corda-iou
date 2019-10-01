# Corda IOU

Corda IOU application leverating `Distributed-Ledger-Technology`

# Setup

### Tools 
* JDK 1.8 latest version

### Running the tests
* When running flow tests you must add the following to your run / debug configuration in the VM options field. This enables us to use
* Quasar - a library that provides high-performance, lightweight threads.
* "-javaagent: /PATH_TO_FILE_FROM_ROOT_DIR/quasar.jar"

# Code Files

## State

* Code: `java-source/src/main/java/net/corda/training/state/IOUState.java`
* Tests: `java-source/src/test/java/net/corda/training/state/IOUStateTests.java`

## Contract

* Code: `java-source/src/main/java/net/corda/training/contract/IOUContract.java`
* Issue Tests: `java-source/src/test/java/net/corda/training/contract/IOUIssueTests.java`
* Transfer Tests: `java-source/src/test/java/net/corda/training/contract/IOUIssueTests.java`
* Settle Tests: `java-source/src/test/java/net/corda/training/contract/IOUIssueTests.java`

## Flow

* Issue code: `java-source/src/main/java/net/corda/training/flow/IOUIssueFlow.java`
* Issue tests: `java-source/src/test/java/net/corda/training/flow/IOUIssueFlowTests.java`
* Transfer code: `java-source/src/main/java/net/corda/training/flow/IOUTransferFlow.java`
* Transfer tests: `java-source/src/test/java/net/corda/training/flow/IOUTransferFlowTests.java`
* Settle code: `java-source/src/main/java/net/corda/training/flow/IOUSettleFlow.java`
* Settle tests: `java-source/src/test/java/net/corda/training/flow/IOUSettleFlowTests.java`

The code in the following files was already added:

* `java-source/src/main/java/net/corda/training/plugin/IOUPlugin.java`
* `java-source/src/test/java/net/corda/training/NodeDriver.java`
* `java-source/src/main/java/net/corda/training/plugin/IOUPlugin.java`
* `java-source/src/main/java/net/corda/training/flow/SelfIssueCashFlow.java`


# Running the CorDapp

* Terminal: Navigate to the root project folder and run `./gradlew java-source:deployNodes`, followed by 
`./java-source/build/node/runnodes`

### Interacting with the CorDapp
Once all the three nodes have started up (look for `Webserver started up in XXX sec` in the terminal), you can interact with the app via a web browser. 
* From a Node Driver configuration, look for `Starting webserver on address localhost:100XX` for the addresses. 

* From the terminal: Node A: `localhost:10009`, Node B: `localhost:10012`, Node C: `localhost:10015`.

To access the front-end gui for each node, navigate to `localhost:XXXX/web/iou/`

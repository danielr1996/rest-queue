# rest-queue
Implementing a queue with pure rest semantics

By cleverly using three HTTP Standards, we can implement a queue like service using pure rest semantics.
On a high level it works by accepting a multipart/form-data payload, which can be submitted as a whole or streamed in by supported applications.
Then it caches the request in memory (or anything that can be represented as a reactor Sink)
The connection is immediatelly closed and returns with 303 SEE OTHER a subscription url where a consumer can then connect to consume the output
Normally http clients follow the Location Header on any 3xx status, so the result can be immedietally consumed
By using text/event-stream as a datatype 


# Features
## Spring Integration
Because rest-queue is written in spring it is as easy as adding the springboot-starter dependency

## Run as standalone service

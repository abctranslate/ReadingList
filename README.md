# ReadingList
Interesting resources from the internet.

# Zen
- Mark ⏳ as looks good but not finished reading yet.
- Mark 👍 as must read.
- Be free to leave your opinion or feeling.
- Never hesitate to delete useless or outdated items.

# Program
## Language
### shell
- ⏳ [Command line text processing with GNU Coreutils](https://learnbyexample.github.io/cli_text_processing_coreutils/preface.html)

### asm
- ⏳ [x86 Assembly Guide](https://www.cs.virginia.edu/~evans/cs216/guides/x86.html)

## Algorithm
### Distributed systems
- 👍 [How to do distributed locking](https://martin.kleppmann.com/2016/02/08/how-to-do-distributed-locking.html)  
  Brief and thought provoking, and also the book 👍 [*Designing Data-Intensive Applications*](https://dataintensive.net/).
- ⏳ [Distributed systems for fun and profit](http://book.mixu.net/distsys/single-page.html)

#### Vector Clock

A basic glance at vector clock

- [Why Vector Clocks Are Easy](https://riak.com/why-vector-clocks-are-easy/)  
- [Why Vector Clocks Are Hard](https://riak.com/posts/technical/why-vector-clocks-are-hard/)  
  A detail I want to add to *Why Vector Clocks Are Hard*:  
  
  > Ben and Cathy were both modifying from the same original object. Since we used their server id instead of their own name to identify the change, Cathy’s message has the same vector clock as Ben’s! This means that Dave’s message (responding to Ben) appears to be a simple successor to Cathy’s… and we lose her data silently!
  
  Why Cathy's data lost? Why not send her data just as the same operation on Ben's data?  
  Because the *Dave* on the image not only means *human Dave*, it actually is *human Dave and Dave's computer*. *Dave's computer* solves all conflicts it can, which are vector clocks that are able to merge with another vector clocks. Only if *Dave's computer* can not do the merge will it hand over the data to *human Dave*. We can see the Cathy's data(X:1, Y:1) is able to merge to Ben's(X:2, Y:1) on *Dave's computer*, and the merged result is Ben's(X:2, Y:1), *human Dave* would never know any data from Cathy, so *we lose her data silently*.

- [Why Cassandra Doesn’t Need Vector Clocks](https://www.datastax.com/blog/why-cassandra-doesnt-need-vector-clocks)  
  Because Cassandra breaks the data into parts, use a UUID as the key, give each write operation a unique key.

- [Version Vectors are not Vector Clocks](https://haslab.wordpress.com/2011/07/08/version-vectors-are-not-vector-clocks/)  
  Version Vectors update casual stats, Vector Clocks determine the total order of events. Furthermore, Vector Clocks never resolve conflicts, only detect them.

### SAT
- [SAT (Separating Axis Theorem)](https://dyn4j.org/2010/01/sat/)

### Computer Graphic
- ⏳ [Introduction to Computer Graphics](https://math.hws.edu/graphicsbook/index.html)

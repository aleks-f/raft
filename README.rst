.. image:: https://travis-ci.org/willemt/raft.png
   :target: https://travis-ci.org/willemt/raft

.. image:: https://coveralls.io/repos/willemt/raft/badge.png
  :target: https://coveralls.io/r/willemt/raft

What?
-----
C implementation of the Raft Consensus protocol, BSD licensed

How does it work?
-----------------
See raft.h for full documentation.

A CRaft user needs to implement all the functions in raft_cbs_t.

Networking is out of scope for this project. The implementor will need to do all the plumbing. *Currently*, this is done by:

- Implementing all the callbacks within raft_cbs_t; and
- Calling raft_recv_* functions with msg_* message structs

Dependencies
------------
There are no dependencies, however https://github.com/willemt/linked-List-queue is required for testing.

Building
--------
$make tests

Todo
----
- Member changes
- Log compaction
- More scenario tests (ie. more varied network partition scenarios)
- Usage example


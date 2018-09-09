# Read-Write-Partition-based-cache-replacement-policy

Implemented Read Write Partition (RWP) based cache replacement policy in C++ which achieved 4.8% overall IPC geometric mean speedup over baseline LRU when run on CPU spec benchmarks.

## Cache replacement policy
Cache memory is limited and for most of the time, only stores the things which will be requiring in future. From the running instruction, it is hard to project the future requirement and thus cache replacement policy plays an important role in evicting only those space from cache which will not be useful in future and improves the performance. Go through the pdf paper for more information.

This Project proposes and implement a cache replacement policy which separates the read write instruction and focus on read instruction to stay in cache and evict the write instruction. Implementation is available in replacement_state.cpp and replacement_state.h.

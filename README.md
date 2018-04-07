# N.Order (Neighborhood Ordering)

N.Order is disk-friendly graph ordering to reduce I/O overhead. In disk-based graph processing, entire graph data is stored into disk. Generally, graph data is arranged by vertex id. Because graph processing workload has extremely random access graph processing on disk-based has low efficiency. N.Order modifies graph layout on disk by re-assigning vertex id. So, it can reduce I/O overhead and improve graph processing performance.

## N.Order`s Goal

1. Optimize graph processing performance by reducing I/O overhead
2. Increase cpu-cache and page-cache hit ratio
3. Minimize graph ordering overhead (especially N.Order has O(|E|) complexity)
4. Especially, N.Order perform well in BFS-like graph algorithms such as BFS, diameter, shortest path and so on

## To-do lists

1. Reduce ordering time through parallel processing
2. Consider parallel graph processing
3. Others...

Refference Gorder(SIGMOD`16) and N.Order(Not published yet).

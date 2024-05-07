# multithreading_102117120

Methodology :
The function multiply_with_threads is created to handle the threading logic. It divides the work among multiple threads and combines the results afterward.
Within multiply_with_threads, a loop creates the specified number of threads (num_threads). 
The matrices are divided into chunks, and each thread works on one chunk independently. This division ensures that each thread operates on a distinct portion of the data, minimizing conflicts.
After starting all the threads, the main thread waits for them to finish using thread.join(). 
The number of threads used (num_threads_list) can be adjusted based on the CPU capabilities and the problem size. 
It is essential to find the optimal number of threads for the given hardware and workload to achieve the best performance.

Graph:
The graph "time taken vs. number of threads" in multithreading illustrates how the execution time varies as the number of threads used in the computation changes.
The graph can be visualized as a line plot, with the number of threads on the x-axis and the corresponding execution time on the y-axis.
Each point on the graph represents the execution time for a specific number of threads. 
There's usually an optimal number of threads beyond which adding more threads doesn't significantly reduce the execution time. This point is influenced by factors such as the number of CPU cores available and the nature of the computation and is called the Optimal Point.
After reaching the optimal point, adding more threads may not result in further reductions in execution time. 

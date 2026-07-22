## 2024-05-24 - GitHub Actions Step Overhead Optimization
**Learning:** GitHub Actions introduces roughly 1-3 seconds of setup and teardown overhead for every distinct step, particularly `run` steps. When a workflow contains multiple separate, sequential `run` blocks doing related file system or environment tasks, this overhead accumulates, making the workflow slower than necessary.
**Action:** Always look to combine sequential bash script `run` blocks into a single step where logically appropriate to eliminate redundant runner step overhead.

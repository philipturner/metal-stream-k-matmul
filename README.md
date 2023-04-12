# Metal String-K Matmul: Breaking the 80% Barrier

Reference: https://arxiv.org/abs/2301.03598

Still theoretical; not proven in practice. This repository was created hastily to make sure the algorithm gets open-sourced before someone tries to copyright it.

TODO: Replace the ZIP with just the Swift script and some instructions to setup the Xcode project.

## Gist:

I can (theoretically) exceed the hardware limit of 80% ALU utilization by switching from FP32 to FP16, and not using `simdgroup_matrix`. The String-K algorithm makes building new GEMM libraries much simpler, such as the FP16 idea. Therefore, I could match and exceed the performance of MPS with every shape and data type, on a reasonable timeline.

1) Unproven but promising way to reach ~90% ALU
2) String-K algorithm which solves a separate problem, but indirectly makes (1) possible

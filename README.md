# mlsys-paper

## Discussion Template

For each paper, we will briefly discuss:

1. What ML system problem is this paper targeting?
2. What is the core motivation?
3. What is the proposed solution?
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

## Seminar on 04/02

### MoE-APEX: An Efficient MoE Inference System with Adaptive Precision Expert Offloading
Conference: ASPLOS 2026
Link: https://dl.acm.org/doi/epdf/10.1145/3779212.3790187

1. What ML system problem is this paper targeting?
2. What is the core motivation?
3. What is the proposed solution?
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

### SuperOffload: Unleashing the Power of Large-Scale LLM Training on Superchips
Conference: ASPLOS 2026
Link: https://arxiv.org/pdf/2509.21271

1. What ML system problem is this paper targeting?
2. What is the core motivation?
3. What is the proposed solution?
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

### IceCache: Memory-Efficient KV-cache Management for Long-Sequence LLMs
Conference: ICLR 2026
Link: https://openreview.net/pdf?id=yHxSKM9kdr

1. What ML system problem is this paper targeting?
    - How to achieve more accurate KV-cache management with lower GPU memory budget in long context reasoning
2. What is the core motivation?
    - Not all tokens are equally important.
       - Although the KV-cache is large,
         the most critical ones for the current generation are usually only a small part of the tokens.
         Therefore, theoretically there is no need to keep all KV on the GPU at every step.
    - Existing offloading / paging method "page selection is not accurate enough"
        - The tokens that are truly relevant to the current query are semantically similar, but may be far apart in time order.
        - So they will be scattered in many pages
        - The system has to load many "pages mixed with a large number of irrelevant tokens",
          resulting in low hit rate, many invalid transmissions, and poor bandwidth utilization.
    - The question is not just "which tokens/pages to choose", but "how to organize these tokens/pages in memory".
        - The question is not just "which tokens/pages to choose", but "how to organize these tokens/pages in memory".
3. What is the proposed solution?
    - It no longer builds pages in the original order of tokens, but clusters similar tokens together based on the semantic similarity of key embeddings.
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

### TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate
Conference: ICLR 2026
Link: https://arxiv.org/pdf/2504.19874

1. What ML system problem is this paper targeting?
2. What is the core motivation?
3. What is the proposed solution?
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

### SpInfer: Leveraging Low-Level Sparsity for Efficient Large Language Model Inference on GPUs
Conference: EuroSys 2025
Link: https://dl.acm.org/doi/10.1145/3689031.3717481

1. What ML system problem is this paper targeting?
2. What is the core motivation?
3. What is the proposed solution?
4. If you were to tackle the same problem, how would you approach it?
5. Does it have potential for edge environments or our research context? If not, why? What are the main barriers?

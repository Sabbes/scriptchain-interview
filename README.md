# scriptchain-interview
1. Suppose that we design a deep architecture to represent a sequence by stacking self-attention layers with positional encoding. What could be issues? (paragraph format)

One problem with stacking layers after positional encoding is that the positional information may be lost in the deeper layers; this can be mitigated by reinjecting the positional encoding at intermediate layers. Furthermore, stacking self-attention layers can cause over-smoothing where the token embeddings converge; this is especially the case for unmastered self-attention layers.
Finally with any stacked layers, computational cost increases with each additional layer, and depending on the sequence being encoded, some of these additional layers may only increase the computation cost without improving the encoding; in the worst case, the depth of the model could cause it to overfit.

2. Can you design a learnable positional encoding method using pytorch? (Create dummy dataset)

The solution is in interview_encoding.
Link to the walkthrough of the solution.

[![Walkthrough](https://img.youtube.com/vi/pNyk34SjrpA/0.jpg)](https://www.youtube.com/watch?v=pNyk34SjrpA)

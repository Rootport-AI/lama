# Lama (GPU-Enhanced Fork)

This is a fork of [advimman/lama](https://github.com/advimman/lama), an awesome open-source inpainting project. We've modified `bin/predict.py` to enable GPU support via command-line arguments, making it faster on systems with CUDA-compatible GPUs like the RTX 4070 Ti SUPER.

## Why This Fork?
The original `predict.py` was hardcoded to use CPU (`device = torch.device("cpu")`), which slowed down inference despite GPU availability. This fork allows you to specify `device=cuda` for blazing-fast performance.

## How to Use
1. Clone this repository:

   git clone https://github.com/Rootport-AI/lama.git

2. Follow the original [LaMa instructions](https://github.com/advimman/lama#quick-start) for setup.
3. Run with GPU: python bin/predict.py model.path=<path-to-checkpoint> indir=<input-dir> outdir=<output-dir> device=cuda

## Acknowledgments
- Huge thanks to [advimman](https://github.com/advimman) and the LaMa team for their amazing work!
- Licensed under Apache 2.0, same as the original (see `LICENSE`).

Happy inpainting!
# 🔍 Qwen2\[.5\]-VL Attention Visualizer


An interactive tool to visualize attention maps for the **Qwen2\[.5\]-VL** vision-language model. It outputs the attention scores on image tokens when generating each text token.

---

## Getting Started

Check out the Jupyter notebook: [`qwenvl.ipynb`](./qwenvl.ipynb)  
It includes an end-to-end example to get you up and running quickly.


## Requirements

Make sure to install the following Python packages:

```bash
pip install torch transformers matplotlib
```

## Notes
- Do **not** install `flash-attn`: it patches the attention block and disables attention score outputs.
- Currently, the vision encoder on `transformers` does not expose attention scores, so this tool does not visualize inner ViT attentions.
- Video inputs are not supported. You need to figure out how the visual tokens correspond to the timestamp and position of the frames.  

## Acknowledgments

- Original visualizer: [LLaVa VLM-Visualizer](https://github.com/zjysteven/VLM-Visualizer)  
- Qwen2\[.5\]-VL model by [Qwen Team / Alibaba](https://github.com/QwenLM/Qwen2.5-VL)

# LLM Fine-Tuning 🎛️

Efficient LLM fine-tuning with LoRA, QLoRA, DPO, and RLHF.

## Methods

| Method | VRAM Required | Speed | Quality |
|--------|-------------|-------|---------|
| Full Fine-tune | 80GB+ | Slow | Best |
| LoRA | 24GB | Fast | Great |
| QLoRA (4-bit) | 8GB | Fast | Good |
| DPO | 24GB | Medium | Best (alignment) |

## Quick Start

```python
from llm_finetune import FineTuner

tuner = FineTuner(
    base_model="meta-llama/Llama-3-8B",
    method="qlora",
    lora_rank=16,
)
tuner.train(dataset=train_data, epochs=3)
tuner.save("my-model/")
```

## License

MIT
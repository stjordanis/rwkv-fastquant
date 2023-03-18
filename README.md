---
license: mit
---

# RWKV fast quant, best used with rwkvstic 2.0.5
## Benchmark
### Nvidia A4000 16GB : 6.0s/100t

# Usage 
```py
from rwkvstic.load import RWKV

# Load the model (supports full path, relative path, and remote paths)

model = RWKV(
    "https://huggingface.co/Hazzzardous/rwkv-fastquant/resolve/main/R14B-8K-FastQuant-rwkvstic-2-0-4.rwkv"
)

model.loadContext(newctx=f"Q: who is Jim Butcher?\n\nA:")
output = model.forward(number=100)["output"]

print(output) 

# Q: who is Jim Butcher?
# A: Jim Butcher is a very popular American author of fantasy novels. He’s known for the Dresden Files series of novels.<|endoftext|>
```
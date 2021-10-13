#### Table of contents
1. [Introduction](#introduction)
2. [Using pretrained with `transformers`](#transformers)

# <a name="introduction"></a> Smaller version XLM-roberta-base for Vietnamese and English


The pre-train language model that was reduced size [Load What You Need](https://arxiv.org/abs/2010.05609)

# <a name="transformers"></a> Using pretrained in [`transformers`](https://github.com/huggingface/transformers)

### Pre-trained models
 
Model | #params 
---|---|
`xlm-roberta-base` | 278M 
`anhtunguyen98/xlm-base-vi-en` | 124M 
`anhtunguyen98/xlm-base-vi` | 117M

### Example usage

```python3
import torch
from transformers import AutoModel, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("anhtunguyen98/xlm-base-vi")
model = AutoModel.from_pretrained("anhtunguyen98/xlm-base-vi")
sentence = 'Tôi là sinh viên PTIT .'  

input_ids = torch.tensor([tokenizer.encode(sentence)])

with torch.no_grad():
    features = model(input_ids)
print(feature)

```

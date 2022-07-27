# Anees Dataset
The dataset used to fine-tune the GPT-2 model used in Anees for the multi-turn dialogue generation.

## Introduction
The dataset is a combination of 4 multi-turn dialogue datasets:
  - DailyDialog: a high-quality multi-turn open-domain English dialog dataset. On average there are around 8 speaker turns per dialogue with around 15 tokens per turn.
  - EmpatheticDialogues: a large-scale multi-turn empathetic dialogue dataset collected on Amazon Mechanical Turk, containing 24,850 one-to-one open-domain conversations.
  - Persona-Chat: crowd-sourced dialogues where each participant plays the part of an assigned persona; and each persona has a word-distinct paraphrase.
  - BlendedSkillTalk: an English-language dataset blending three conversation skills in balanced proportions (demonstrating knowledge, empathy, or ability to talk about oneself).

## Analysis

| Dataset               | # of training dialogues | # of training utterances | # of validation dialogues | # of validation utterances |
| --------------------- | ----------------------- | ------------------------ | ------------------------- | -------------------------- |
| DailyDialog | 11150 | 87467 | 1968 | 15512 |
| EmpatheticDialogues | 19628 | 84674 | 3464 | 14912 |
| Persona-Chat | 16046 | 212873 | 2832 | 37788 |
| BlendedSkillTalk | 5786 | 76435 | 1022 | 13482 |
| Total | 52610 | 461449 | 9286 | 81694 |

## Tokenization and Translation
  - The English dataset was tokenized using the [GPT2 Tokenizer](https://huggingface.co/gpt2).
  - The Arabic dataset was tokenized using the [AraGPT2 Tokenizer](https://huggingface.co/aubmindlab/aragpt2-base).
  - The translation from English to Arabic was done using [Opus-MT](https://huggingface.co/Helsinki-NLP/opus-mt-ar-en) on [Colab](https://colab.research.google.com/drive/1d-ynR5qfv22zRwRs3QNLKC8-s0ux2PRC?usp=sharing).
  - The preprocessing and loading details of the data can be found on [Anees repository](https://github.com/aashrafh/Anees).
  
## References
  - [Li, Y., Su, H., Shen, X., Li, W., Cao, Z., & Niu, S. (2017). Dailydialog: A manually labelled multi-turn dialogue dataset. arXiv preprint arXiv:1710.03957.](https://arxiv.org/abs/1710.03957)
  - [Rashkin, H., Smith, E. M., Li, M., & Boureau, Y. L. (2018). Towards empathetic open-domain conversation models: A new benchmark and dataset. arXiv preprint arXiv:1811.00207.](https://arxiv.org/abs/1811.00207)
  - [Zhang, S., Dinan, E., Urbanek, J., Szlam, A., Kiela, D., & Weston, J. (2018). Personalizing dialogue agents: I have a dog, do you have pets too?. arXiv preprint arXiv:1801.07243.](https://arxiv.org/abs/1801.07243)
  - [Smith, E. M., Williamson, M., Shuster, K., Weston, J., & Boureau, Y. L. (2020). Can You Put it All Together: Evaluating Conversational Agents' Ability to Blend Skills. arXiv preprint arXiv:2004.08449.](https://arxiv.org/abs/2004.08449)

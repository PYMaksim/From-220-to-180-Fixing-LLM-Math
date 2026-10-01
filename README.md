# LLM Math Reasoning Benchmark: YandexGPT vs GigaChat

## 📊 Executive Summary
Comparative analysis of mathematical reasoning capabilities between **YandexGPT 5 Pro** and **GigaChat** (Sber). 
**Finding:** Both models fail at Zero-Shot math, requiring explicit "Chain of Thought" (CoT) prompting for 100% accuracy.

## 📈 Benchmark Results

| Test Case | YandexGPT 5 Pro | GigaChat | Winner |
| :--- | :--- | :--- | :--- |
| **Zero-Shot (RU)** | ❌ **Fail** (220) | ❌ **Fail** (140) | — |
| **Zero-Shot (EN)** | ❌ **Fail** (220) | ❌ **Fail** (220) | — |
| **Chain of Thought (RU)** | ✅ **Pass** (180) | ✅ **Pass** (180) | Tie |
| **Chain of Thought (EN)** | ✅ **Pass** (180) | ✅ **Pass** (180) | Tie |
| **Latency (CoT RU)** | **~2.6s** | ~4.1s | 🟢 YandexGPT |
| **Latency (CoT EN)** | ~3.1s | ~3.5s | 🟢 YandexGPT |
| **Output Format** | LaTeX / Rich Text | Plain Text / Markdown | YandexGPT |

## 💡 Key Takeaways

1.  **Zero-Shot is unreliable:** Both models failed basic arithmetic without guidance. YandexGPT ignored the quantity of items, GigaChat ignored the prices.
2.  **Chain of Thought is mandatory:** Adding "Solve step-by-step" increased accuracy from **0% to 100%**.
3.  **Performance:** YandexGPT demonstrated ~30-40% faster inference speed in reasoning tasks compared to GigaChat.
4.  **Formatting:** YandexGPT natively outputs LaTeX for formulas, which is superior for technical documentation.

## 🛠 Conclusion
For production math tasks, **CoT prompting is non-negotiable**. YandexGPT shows superior latency and formatting capabilities in this test.

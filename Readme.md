
# Edge AI Quantized Models Benchmark

This project demonstrates an **Edge AI pipeline** for deploying and benchmarking quantized ML models on **low-power devices like Raspberry Pi**. The focus is on reducing memory usage and improving inference latency using **dynamic INT8 quantization**.

---

## Features
- Load FP32 models: **MobileNetV2** (Conv-heavy) and **LSTM** (Linear-heavy)  
- Apply **dynamic INT8 quantization** via TorchScript  
- Benchmark **latency** and **memory usage** for FP32 vs INT8  
- Visualize results using **Matplotlib**  
- Deployment-ready for **Raspberry Pi / low-power devices**

---

## Setup

Install dependencies:

```bash
pip install torch torchvision matplotlib psutil numpy<2
```

---

## Run Pipeline in Colab

Everything can be run inside a single Colab notebook:

1. **Load FP32 models**  
2. **Quantize models to INT8**  
3. **Benchmark all models**  
4. **Visualize results**

> The notebook runs all steps sequentially and generates side-by-side plots for MobileNetV2 and LSTM.

---

## Sample Results

| Model        | FP32 Time | FP32 Mem | INT8 Time | INT8 Mem |
|-------------|-----------|----------|-----------|----------|
| MobileNetV2 | 62.04 ms  | 37.29 MB | 46.91 ms  | 10.18 MB |
| LSTM        | 2.73 ms   | 2.75 MB  | 2.73 ms   | 0.00 MB  |

- **Memory reduction**: MobileNetV2 ≈ 73%  
- **Latency improvement**: MobileNetV2 ≈ 13%  
- **LSTM performance**: latency maintained, memory reduced

---

## Key Highlights
- PyTorch, TorchScript, dynamic quantization  
- Edge AI deployment pipelines  
- Performance profiling (latency & memory)  
- Visualization with Matplotlib  
- Deployment-ready for Raspberry Pi / low-power devices

---

## Colab Link

Run the notebook directly in Colab:

[Open in Colab](https://colab.research.google.com/github/vikesh3640/edge_ai/blob/main/EdgeAi.ipynb)

---


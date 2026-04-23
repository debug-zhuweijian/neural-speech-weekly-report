# 神经语音信号处理周报配套代码

本目录与以下两个文件同步维护：

- `../weekly-report.md`
- `../mathtype-formulas.md`

目标是保持三者在以下方面一致：

- 数学对象一致
- 变量命名一致
- 数值示例一致
- 代码输出能支撑周报里的结论

## 代码索引

| 文件名 | 验证目标 | 对应周报章节 | 对应公式 |
|--------|----------|--------------|----------|
| dft_basic.py | DFT 单边幅度谱与周期图 | 一.1 时域到频域 | M-01 |
| stft_demo.py | 离散 STFT 分帧与峰值频率迁移 | 一.1 时域到频域 | M-02 |
| mel_filterbank.py | Hz/Mel 互换与三角滤波器组 | 一.2 感知频率压缩 | M-03 |
| dct_ii_demo.py | DCT-II 正交归一化与重构 | 一.3 MFCC 与动态特征 | M-04 |
| mfcc_delta.py | Delta / Delta-Delta 回归差分 | 一.3 MFCC 与动态特征 | A-01 |
| hilbert_envelope.py | Hilbert 解析信号与包络 | 二.2 包络提取与标准化 | M-05 |
| notch_filter.py | 二阶 IIR 陷波滤波 | 二.1 预处理管线 | A-02 |
| car_demo.py | CAR 公共平均参考 | 二.1 预处理管线 | M-06 |
| bandpass_filter.py | Butterworth 带通滤波 | 二.1 预处理管线 | M-07 |
| zscore_demo.py | Z-score 标准化 | 二.2 包络提取与标准化 | M-08 |
| feature_matrix_demo.py | T x C 特征矩阵构建 | 二.2 包络提取与标准化 | M-05, M-08 |
| rnn_gradient.py | RNN 隐状态衰减与梯度消失 | 三.1 RNN → LSTM → BiLSTM | M-09 |
| lstm_cell.py | LSTM 门控与状态保持 | 三.1 RNN → LSTM → BiLSTM | M-10, M-11 |
| bilstm_context.py | BiLSTM 双向上下文 | 三.1 RNN → LSTM → BiLSTM | M-09, M-11 |
| ctc_alignment.py | CTC 路径枚举与边际概率 | 三.2 时序对齐 | A-03 |
| conv1d_demo.py | 1D 卷积输出长度与因果填充 | 三.3 卷积基础 | A-04 |
| dilated_causal_conv.py | 膨胀因果卷积感受野 | 三.3 卷积基础 | A-05 |

## 运行依赖

- Python 3.8+
- `numpy`
- `scipy`（仅 `bandpass_filter.py` 需要）

## 使用方式

```bash
python dft_basic.py
python stft_demo.py
python mfcc_delta.py
```

每个脚本都可以独立运行，输出的文字说明已经按周报口径统一。

# 千言：面向事实一致性的文本生成比赛

> 百度"千言"数据集系列竞赛 —— 事实一致性文本生成任务

## 项目简介

本项目参加百度"千言"计划的事实一致性文本生成评测任务，基于 **PaddlePaddle** 深度学习框架，使用 **UNIMO** 预训练模型进行广告文案自动生成，并结合 **DuReaderQG** 模型实现问题生成增强。

## 技术路线

- **模型架构**：UNIMO（统一模态预训练模型）+ DuReaderQG
- **框架**：PaddlePaddle 2.x + PaddleNLP
- **任务类型**：Conditional Text Generation（条件文本生成）
- **训练数据**：AdvertiseGen 广告文案生成数据集
- **评估指标**：BLEU、事实一致性评分

## 核心模块

1. **数据预处理**：训练数据加载、清洗、格式转换、产品类型统计
2. **模型微调**：基于 UNIMO 的 AdvertiseGen 广告文案生成微调
3. **问题生成增强**：使用 DuReaderQG 进行阅读理解问题生成，扩充数据
4. **后处理优化**：重复检测、长度控制、质量过滤
5. **结果提交**：生成 `l.adv_optimized.txt` 提交文件

## 文件说明

```
.
├── README.md                      # 本文件
├── main.ipynb                     # 主程序（Jupyter Notebook）
└── requirements.txt               # 依赖项
```

## 环境要求

- Python 3.7+
- PaddlePaddle 2.x (GPU 版本推荐)
- PaddleNLP 2.0.8
- numpy, tqdm

## 快速开始

```bash
# 安装依赖
pip install paddlenlp==2.0.8 paddlepaddle-gpu numpy tqdm

# 运行 Notebook
jupyter notebook main.ipynb
```

## 许可证

本项目仅用于学术交流与学习参考。

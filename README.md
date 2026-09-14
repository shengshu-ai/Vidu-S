# Vidu S

<div align="center" style="line-height: 1;">
  <a href="https://www.vidu.com/vidu-stream">
    <img alt="Try Vidu S2"
      src="https://img.shields.io/badge/Try-Vidu%20S2-555555?labelColor=00a67d&color=555555&logo=googlegemini&logoColor=white" height="32"/>
  </a>
  <a href="https://arxiv.org/abs/2609.11638">
    <img alt="Vidu S2 Paper"
      src="https://img.shields.io/badge/Vidu%20S2%20Paper-arXiv%3A2609.11638-555555?labelColor=b31b1b&color=555555&logo=arxiv&logoColor=white" height="32"/>
  </a>
  <a href="https://arxiv.org/abs/2607.03118">
    <img alt="Vidu S1 Paper"
      src="https://img.shields.io/badge/Vidu%20S1%20Paper-arXiv%3A2607.03118-555555?labelColor=b31b1b&color=555555&logo=arxiv&logoColor=white" height="32"/>
  </a>
  <a href="https://shengshu.feishu.cn/wiki/X7ZLwyLUzi461LkAlNpcTxs1nsy">
    <img alt="English Documentation"
      src="https://img.shields.io/badge/Docs-English-555555?labelColor=2f6fed&color=555555&logo=readthedocs&logoColor=white" height="32"/>
  </a>
  <a href="https://shengshu.feishu.cn/wiki/Fz8ywkzEwil84LkbCOKcxotMnvb">
    <img alt="Chinese Documentation"
      src="https://img.shields.io/badge/Docs-Chinese-555555?labelColor=0891b2&color=555555&logo=readthedocs&logoColor=white" height="32"/>
  </a>
  <a href="https://platform.vidu.com/vidu-stream/doc">
    <img alt="English API Documentation"
      src="https://img.shields.io/badge/API%20Docs-English-555555?labelColor=7c3aed&color=555555&logo=fastapi&logoColor=white" height="32"/>
  </a>
  <a href="https://platform.vidu.cn/vidu-stream/doc">
    <img alt="Chinese API Documentation"
      src="https://img.shields.io/badge/API%20Docs-Chinese-555555?labelColor=7c3aed&color=555555&logo=fastapi&logoColor=white" height="32"/>
  </a>
</div>

<p align="center">
  <img src="figures/vidu-s2-overview.png" alt="Vidu S2 Overview" width="100%">
</p>

## Introduction

### Vidu S2

Vidu S2 extends real-time video generation beyond talking-head digital characters to high-resolution interactive avatars, live video editing, and immersive spatial video. It includes **Vidu S2-Avatar** for controllable character generation and **Vidu S2-Editing** for transforming incoming video streams, both designed for continuous, low-latency interaction.

Key breakthroughs:
1. **720p real-time interactive avatars**
   - Vidu S2-Avatar generates 720p video at **25–42 FPS**, follows a wider range of instructions—including large body motions such as dancing—and accepts new reference images at any moment during a stream.
2. **Stable long-horizon generation with Self-Replay Forcing**
   - Self-Replay Forcing (SRF) replays re-noised, self-generated trajectories in a gradient-enabled causal pass, helping prevent errors from accumulating across streaming segments.
3. **Real-time editing of incoming video**
   - Vidu S2-Editing supports style transfer, virtual try-on, character replacement, and background replacement from text instructions and optional reference images while preserving the source motion and timing.
4. **Real-time spatial video for immersive displays**
   - Generated or edited streams can be converted into synchronized left- and right-eye views, while stereoscopic inputs can be edited jointly for streaming to VR headsets.
5. **Efficient inference on low-cost GPUs**
   - An optimized serving stack combines efficient attention, low-bit GEMM, kernel and launch optimizations, and multi-GPU pipelining to meet real-time inference requirements.

### Vidu S1

Vidu S1 is a real-time interactive video generation model for voice-controlled digital characters. Users can guide generated video content at any moment through spoken instructions, enabling live interaction.  

Key breakthroughs:
1. **Real-time speech control over video content**
   - Users can directly instruct digital characters to perform actions.
2. **Infinite-length real-time interactive generation**
   - Vidu S1 generates 540p video at up to **42 FPS** and can run on consumer GPUs.
3. **Custom character images and voice tones**
   - Vidu S1 supports real people, anime-style characters, pets, and other personalized avatars.

## Quick Links

### Vidu S2

- **Try Vidu S2**: https://www.vidu.com/vidu-stream
- **Vidu S2 Paper**: https://arxiv.org/abs/2609.11638

### Vidu S1

- **Vidu S1 Paper**: https://arxiv.org/abs/2607.03118

## Docs

### Vidu S2

#### English

- **User Guide**: [shengshu.feishu.cn/wiki/X7ZLwyLUzi461LkAlNpcTxs1nsy](https://shengshu.feishu.cn/wiki/X7ZLwyLUzi461LkAlNpcTxs1nsy)
- **API Documentation**: [platform.vidu.com/vidu-stream/doc](https://platform.vidu.com/vidu-stream/doc)
- **API Quickstart**: [platform.vidu.com/vidu-stream/doc/s2-avatar/realtime/quick-start](https://platform.vidu.com/vidu-stream/doc/s2-avatar/realtime/quick-start)

#### Chinese

- **User Guide**: [shengshu.feishu.cn/wiki/Fz8ywkzEwil84LkbCOKcxotMnvb](https://shengshu.feishu.cn/wiki/Fz8ywkzEwil84LkbCOKcxotMnvb)
- **API Documentation**: [platform.vidu.cn/vidu-stream/doc](https://platform.vidu.cn/vidu-stream/doc)
- **API Quickstart**: [platform.vidu.cn/vidu-stream/doc/s2-avatar/realtime/quick-start](https://platform.vidu.cn/vidu-stream/doc/s2-avatar/realtime/quick-start)

<!--
#### Agent Skill

For agent-assisted API integration, use the `vidu-s1-api` Skill. In Claude Code, Codex, OpenClaw, or any agent that supports Skills, say directly:

```text
Install this skill: https://github.com/shengshu-ai/vidu-s-api/tree/main/skills/vidu-s1-api
```

The agent will clone and install it into the proper Skills directory. Restart the agent if required, then ask it to load `vidu-s1-api` for Vidu S1 API integration.
-->

## Updates

- **[2026-09]**: Vidu S2 is now available to try at [vidu.com/vidu-stream](https://www.vidu.com/vidu-stream)
- **[2026-07]**: Vidu S1 is now available.

## Citation

If you find Vidu S useful for your research, please cite:

```bibtex
@misc{zhang2026vidus2realtimeinteractive,
  title={Vidu S2: Real-Time Interactive, Editable, and Spatial Video Generation},
  author={Jintao Zhang and Kai Jiang and Jintao Chen and Xu Wang and Deyuan Liu and Jungang Li and Dechuang Chen and Ming Lin and Jingjiang Zhou and Haopeng Jin and Qi Jia and Xiaohang Wang and Yaole Wang and Zhanqiang Zhang and Ran Li and Zhengkun Huang and Shuyue Xiong and Yuji Wang and Zikun Dai and Hui He and Yang Luo and Mang Ning and Weiqi Feng and Chengyang Ye and Xinyue Lin and Min Zhao and Hongzhou Zhu and Hengkai Tan and Zeyuan Wang and Chendong Xiang and Kaiwen Zheng and Zhijie Deng and Fan Bao and Jianfei Chen and Jun Zhu},
  year={2026},
  eprint={2609.11638},
  archivePrefix={arXiv},
  primaryClass={cs.CV},
  url={https://arxiv.org/abs/2609.11638},
}
```

```bibtex
@article{zhang2026vidu,
  title={Vidu S1: A Real-Time Interactive Video Generation Model},
  author={Zhang, Jintao and Jiang, Kai and Chen, Jintao and Wang, Xu and Luo, Yang and Wang, Yuji and Chen, Dechuang and Li, Jungang and Ye, Chengyang and Chen, Marco and others},
  journal={arXiv preprint arXiv:2607.03118},
  year={2026}
}
```

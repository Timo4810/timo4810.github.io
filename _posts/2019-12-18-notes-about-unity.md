---
layout: article
title: Hello, world.
tag:
    - 游戏制作
    - Unity
---

见链接中2018年10月的回答
https://answers.unity.com/questions/25139/how-i-can-change-the-speed-of-a-song-or-sound.html

* 目前不适用于WebGL，因Audio Mixer不被支持。

---

1. 添加一个Audio Mixer Group
2. 将Audio Source的outputAudioMixerGroup设为刚添加的Audio Mixer Group
3. 在这个Audio Mixer Group中加入Pitch Shifter效果
4. 将Pitch Shifter的Pitch参数暴露到脚本中
5. 若使播放速度变为原来的x倍
    1. 将Audio Source的pitch参数乘x
    2. 将Pitch Shifter的pitch参数除x
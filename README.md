# cartoon-mv-skill

**2D cartoon music videos and story shorts, generated entirely in code — an open-source skill for AI coding agents.**

An open-source skill in the Agent Skills (`SKILL.md`) format that teaches an AI coding agent how to produce a complete cartoon MV or story short from a song or a script: every character, prop and environment drawn in SVG/CSS/Canvas, semantic storyboarding driven by the lyrics, multi-angle cinematic camera work, rendered to 1920×1080 MP4 with SVG + GSAP + Puppeteer + FFmpeg. Zero external assets.

## What it does

- **Cinematic by default.** 16:9 widescreen, 1920×1080, 30 fps, MP4 (H.264 + AAC)
- **18 camera positions, 20 camera moves.** Front, profile, three-quarter, back view, top-down, low angle, over-the-shoulder, POV, split screen… tracking shots, orbits, whip pans, impact push-ins — every shot records a `semanticReason` and a `cameraReason`, so the camera work is motivated, not random
- **Semantic storyboarding.** Lyrics or script lines drive the characters, props, environment, lighting and camera of each shot, cut on the real vocal timeline
- **Smart duration.** Measured from the audio with FFprobe when there is a song; estimated from speech rate and punctuation for narration — never a hard-coded 10/30/60 seconds
- **12 switchable art styles.** Healing, cyberpunk, American comics, anime, ink wash, Chinese national style…
- **Characters that stay alive.** Walk/run cycles, breathing, blinking, scarf and hair motion — nobody stands frozen mid-song

## Case study

**Wang Leehom — 《爱错》 (Love Wrong):** 238.83 s of original audio, 38 precisely timestamped lyric lines, a 28-shot cut with walk/run cycles, breathing and blinking, flowing scarves and a spinning dance sequence — native 16:9, filling the frame edge to edge.

Companion skills by the same author: [interactive-mv-skill](https://github.com/wdu496132-rgb/interactive-mv-skill) — interactive web MVs with karaoke lyrics and branching endings — and pixel-mv-skill (pixel-art MVs, publication in progress). Together they cover the interactive, cartoon and pixel-art styles of code-generated music video.

## Install

Clone this repo into your agent's skills directory, e.g. for Muse:

```bash
git clone https://github.com/wdu496132-rgb/cartoon_mv ~/workspace/custom-skills/cartoon-mv
```

`SKILL.md` follows the open Agent Skills format used by Muse, Claude Code, Codex and other compatible agents. Then just ask your agent: *"Make a cartoon MV for this song."*

## Files

- `SKILL.md` — the skill itself: the complete V2.2 production spec and master prompt
- `skill.yaml` — skill metadata
- `LICENSE` — MIT License

## License

MIT © 2026 Du Wei ([@wdu496132-rgb](https://github.com/wdu496132-rgb))

---

## 中文说明

一个可复用的开源 Skill：**用纯代码制作二维卡通 MV / 剧情短片**（V2.2）。

给一首歌（音频 + 歌词）或一段文案，生成纯代码绘制的二维卡通视频：

- **默认 16:9 横屏**，1920×1080，30fps，MP4（H.264 + AAC）
- **多视角多机位**：18 种机位/景别（正面、侧面、3/4、背影、俯视、仰视、越肩、主观、分屏……），20 类运镜（跟拍、环绕、甩镜、冲击推近……）
- **语义分镜**：歌词/文案驱动人物、道具、环境、光影、镜头，每镜头有 `semanticReason` + `cameraReason`
- **智能时长**：有音频按 FFprobe 实测时长，无音频按语速标点估算，绝不写死 10/30/60 秒
- **12 种可切换美术风格**：治愈、赛博、美漫、日漫、水墨、国风……
- 零外部素材：角色场景全部由 SVG/CSS/Canvas 代码绘制

**实测案例：** 王力宏《爱错》卡通 MV——238.83 秒原音频驱动，38 句精确歌词时间轴，28 镜头版含走路/奔跑循环、呼吸眨眼、围巾飘动、共舞旋转，原生 16:9 撑满全屏。

**安装：** 把本仓库放到 Muse 的 custom skills 目录（见上方英文命令），之后对 AI 说"做个卡通 MV"即可按 V2.2 规范开工。

**许可证：** MIT

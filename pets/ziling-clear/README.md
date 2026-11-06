# 紫玲（清晰）

白发紫瞳的龙角女仆，明亮紫色服装与白皙肤色，陪你专注工作。

## 预览

![四个状态画面](previews/four-stills.png)

![状态动画](previews/all-states.gif)

[MP4 预览](previews/all-states.mp4) · [全部帧总览](previews/contact-sheet.png) · [十六方向总览](previews/direction-sheet.png)

![待机—跳跃—待机](previews/idle-jump-idle.gif)

![看向循环](previews/look-loop.gif)

## 文件用途

| 文件 | 用途 |
| --- | --- |
| `spritesheet.png` | 最终透明 PNG 图集，用于支持该图集规格的宠物创建工具 |
| `reference.png` | 已确认的完整角色立绘；绿色是制作时的抠图底色 |
| `metadata.json` | 名称、描述、尺寸、帧数与文件摘要；属于本仓库的资料清单 |
| `previews/` | 九组状态 GIF、综合 GIF/MP4、看向循环、跳跃衔接及静态总览 |
| `validation/` | 实际运行得到的结构、质量、方向、连续性与边缘清理报告 |
| `checksums.sha256` | 文件校验值 |

## 图集规格

- v2，1536 × 2288 像素，8 列 × 11 行。
- 每格 192 × 208 像素，73 个有效帧；15 个未使用格完全透明。
- SHA-256：`73a51251e274322a4ece95551ad42f812ba0252a00686afc5cd79c07fc5bfe44`。

| 行（从 0 开始） | 状态 | 帧数 |
| --- | --- | ---: |
| 0 | 待机 idle | 6 |
| 1 | 向右移动 running-right | 8 |
| 2 | 向左移动 running-left | 8 |
| 3 | 挥手 waving | 4 |
| 4 | 跳跃 jumping | 5 |
| 5 | 受挫 failed | 8 |
| 6 | 等待输入 waiting | 6 |
| 7 | 工作/思考 running | 6 |
| 8 | 检查成果 review | 6 |
| 9 | 顺时针看向 000°–157.5° | 8 |
| 10 | 顺时针看向 180°–337.5° | 8 |

## 使用

下载 `spritesheet.png`，在支持上述图集规格的宠物创建工具中上传该文件，名称填写“紫玲（清晰）”，描述可使用本页第一段。

本仓库保存可移植的素材。下载文件不会自动把宠物安装到应用中；`metadata.json` 也不是安装程序。桌面交互能力由目标应用提供。

## 校验记录

最终文件通过图集结构检查、质量检查及宠物服务创建前校验。跳跃离地 28 像素，落地基线与待机一致；看向中心最大偏移 1.5 像素。

独立方向盲审的四个基本看向均通过。157.5° 和 202.5° 的姿态接近向下，左右偏转较细微；有标签循环复核后保留为警告，详见 `validation/directions.json` 和 `validation/blind-validation.json`。

图像由 OpenAI 内置图像生成工具按参考形象与用户确认的修改制作，再通过确定性脚本提取、组装并清理边缘。预览全部来自本目录的最终图集。

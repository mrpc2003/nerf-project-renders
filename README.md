<div align="center">

# 🌌 NeRF Project Renders

<img src="rgb/frame_00088.png" alt="NeRF render — hero frame" width="300" />

**Neural Radiance Fields 렌더 결과물 — 이미지 아카이브**

<sub>A small gallery of <code>nerfacto</code> render screenshots — RGB &amp; depth frames.</sub>

<br/>

[![Type](https://img.shields.io/badge/Repo-Render%20Artifacts-8A2BE2?style=flat-square)](#-about)
[![Frames](https://img.shields.io/badge/Frames-5%20RGB%20%2B%202%20Depth-1f6feb?style=flat-square)](#-frame-index)
[![Resolution](https://img.shields.io/badge/Resolution-540%C3%97960-2ea44f?style=flat-square)](#-frame-index)
[![Framework](https://img.shields.io/badge/Pipeline-nerfacto-orange?style=flat-square)](#-references)
[![Format](https://img.shields.io/badge/Format-PNG-lightgrey?style=flat-square)](#-repository-structure)

</div>

---

## 📑 Table of Contents

- [📖 About](#-about)
- [🖼️ Gallery](#%EF%B8%8F-gallery)
- [🌗 RGB ↔ Depth Pairs](#-rgb--depth-pairs)
- [🗂️ Frame Index](#%EF%B8%8F-frame-index)
- [📁 Repository Structure](#-repository-structure)
- [🧭 Usage Notes](#-usage-notes)
- [🧪 References](#-references)
- [👤 Maintainer](#-maintainer)

---

## 📖 About

이 레포지토리는 **NeRF (Neural Radiance Fields) 렌더 출력 PNG** 만을 보관하는 *아티팩트 아카이브*입니다.
학습 코드, 데이터셋, 카메라 포즈, 체크포인트는 포함되어 있지 **않습니다**.

| 항목 | 내용 |
|---|---|
| 🎯 **목적** | 발표 자료 · 노션 페이지 · 블로그에 직접 임베드할 정적 이미지 호스팅 |
| 📦 **내용물** | NeRF 학습 후 카메라 경로를 따라 렌더링한 RGB / Depth 프레임 |
| 🧰 **파이프라인** | `nerfacto` 출력 *(commit history 근거)* |
| 🚫 **비포함** | 학습 코드, 원본 영상/이미지, 카메라 캘리브레이션, 모델 가중치 |

> 본 레포만으로 학습/재현은 불가능하며, 결과물의 시각적 결과를 빠르게 확인하거나 외부 문서에 삽입하는 용도로 설계되었습니다.

---

## 🖼️ Gallery

총 5장의 RGB 렌더 컷입니다. *(540 × 960, portrait)*

<table>
  <tr>
    <td align="center"><img src="rgb/frame_00001.png" width="180" alt="frame 00001" /><br/><sub><b>frame_00001</b></sub></td>
    <td align="center"><img src="rgb/frame_00044.png" width="180" alt="frame 00044" /><br/><sub><b>frame_00044</b></sub></td>
    <td align="center"><img src="rgb/frame_00088.png" width="180" alt="frame 00088" /><br/><sub><b>frame_00088</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="rgb/frame_00132.png" width="180" alt="frame 00132" /><br/><sub><b>frame_00132</b></sub></td>
    <td align="center"><img src="rgb/frame_00177.png" width="180" alt="frame 00177" /><br/><sub><b>frame_00177</b></sub></td>
    <td align="center"><sub>— end of sequence —</sub></td>
  </tr>
</table>

---

## 🌗 RGB ↔ Depth Pairs

동일 프레임 번호로 매칭되는 컬러(RGB)와 깊이(Depth) 출력입니다.

<table>
  <tr>
    <th align="center">Frame</th>
    <th align="center">RGB</th>
    <th align="center">Depth</th>
  </tr>
  <tr>
    <td align="center"><b><code>00044</code></b></td>
    <td align="center"><img src="rgb/frame_00044.png" width="260" alt="rgb 00044" /></td>
    <td align="center"><img src="depth/frame_00044.png" width="260" alt="depth 00044" /></td>
  </tr>
  <tr>
    <td align="center"><b><code>00132</code></b></td>
    <td align="center"><img src="rgb/frame_00132.png" width="260" alt="rgb 00132" /></td>
    <td align="center"><img src="depth/frame_00132.png" width="260" alt="depth 00132" /></td>
  </tr>
</table>

---

## 🗂️ Frame Index

| Frame   | RGB | Depth | 비고 |
|:-------:|:---:|:-----:|:-----|
| `00001` | ✅  |  —   | 시퀀스 시작 |
| `00044` | ✅  |  ✅  | RGB ↔ Depth 페어 |
| `00088` | ✅  |  —   | — |
| `00132` | ✅  |  ✅  | RGB ↔ Depth 페어 |
| `00177` | ✅  |  —   | 시퀀스 끝 |

**합계** : RGB 5장 · Depth 2장 · 총 7개의 PNG.

---

## 📁 Repository Structure

```text
nerf-project-renders/
├── rgb/                       # 색상(RGB) 렌더 출력
│   ├── frame_00001.png
│   ├── frame_00044.png
│   ├── frame_00088.png
│   ├── frame_00132.png
│   └── frame_00177.png
└── depth/                     # 깊이(Depth) 렌더 출력
    ├── frame_00044.png
    └── frame_00132.png
```

---

## 🧭 Usage Notes

### 외부 문서에 임베드 (Notion · 블로그 · 슬라이드)

GitHub raw URL 을 그대로 이미지로 사용할 수 있습니다.

```markdown
![NeRF render — frame 88](https://raw.githubusercontent.com/mrpc2003/nerf-project-renders/master/rgb/frame_00088.png)
```

```html
<img src="https://raw.githubusercontent.com/mrpc2003/nerf-project-renders/master/depth/frame_00132.png" width="480" />
```

### 로컬에서 모두 받기

```bash
git clone https://github.com/mrpc2003/nerf-project-renders.git
cd nerf-project-renders
```

<details>
<summary>📌 새 렌더를 추가할 때 권장 컨벤션</summary>

- 파일명은 `frame_<5자리 숫자>.png` (예: `frame_00088.png`)
- RGB 렌더는 `rgb/`, Depth 렌더는 `depth/` 디렉터리에 보관
- 가능하면 같은 프레임 번호로 **RGB ↔ Depth 페어**를 유지하면 비교 표가 깔끔하게 채워집니다.

</details>

---

## 🧪 References

- 본 레포의 결과물은 `nerfacto` 파이프라인 출력으로 식별됩니다. *(commit message 근거)*
- [nerfstudio](https://github.com/nerfstudio-project/nerfstudio) — `nerfacto` 를 포함하는 NeRF 학습/렌더링 프레임워크.

> ⚠️ 학습 코드와 씬 데이터는 본 레포에 포함되어 있지 않으므로, 위 프레임워크만으로 같은 결과를 그대로 재현할 수는 없습니다.

---

<div align="center">

## 👤 Maintainer

**김우현** &middot; [`@mrpc2003`](https://github.com/mrpc2003)

<sub>📷 NeRF render artifacts — image archive only.</sub>

</div>

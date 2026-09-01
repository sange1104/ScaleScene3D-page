# ScaleScene3D-page

Official project page for **ScaleScene3D: Scaling 3D Generative Priors to Large-Scale Scene Meshes from Multi-View Images**.

🌐 https://sange1104.github.io/ScaleScene3D-page/

## Structure

```
index.html                  # 페이지 본문 (여기만 고치면 됩니다)
static/css/hybrid.css       # 스타일 (라이트/다크 자동)
static/images/              # intro_v2.jpg, method_v2.jpg, results_poster.jpg
static/videos/              # scalability_and_large_scale_results.mp4 (웹 최적화본, 38MB)
originals/                  # 원본 영상 (88MB) — .gitignore 처리, 커밋되지 않음
CONTENT.md                  # 작업용 콘텐츠 메모 — .gitignore 처리, 로컬 전용
```

영상 재인코딩 시:

```bash
ffmpeg -i originals/scalability_and_large_scale_results_original.mp4 \
  -c:v libx264 -preset slow -crf 25 -pix_fmt yuv420p -profile:v high \
  -g 60 -movflags +faststart -an \
  static/videos/scalability_and_large_scale_results.mp4
```

## Local preview

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Deploy (GitHub Pages)

Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)`

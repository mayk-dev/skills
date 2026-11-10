# SKILL.md — Criador de Vídeos Virais Animados em HTML5

## 🎯 Objetivo

Criar animações HTML5 autocontidas (single-file) para vídeos virais curtos
(Shorts/Reels/TikTok) ou animações narrativas, com:
- VFX visuais em Canvas 2D
- Áudio gerado por Web Audio API (sem arquivos externos)
- Legendas estilo TikTok/CapCut
- Gravação automática em vídeo (MediaRecorder)
- Painel de controle + narração sincronizada

---

## 📐 Formatos de Tela (Canvas)

| Formato | Resolução | Uso |
|---------|-----------|-----|
| Vertical | `1080 × 1920` | YouTube Shorts, Reels, TikTok |
| Quadrado | `1080 × 1080` | Feed Instagram, LinkedIn |
| Horizontal | `1920 × 1080` | YouTube normal, apresentações |
| Panorâmico | `960 × 600` | Demonstração em desktop |

Sempre definir no `<canvas width="X" height="Y">` e usar as constantes `W` e `H`.

---

## 🏗️ Estrutura Base (esqueleto do HTML)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Título do Vídeo</title>
  <style> /* estilos do stage + painel + HUD */ </style>
</head>
<body>
  <div class="stage">
    <canvas id="c" width="1080" height="1920"></canvas>
    <div class="side-panel"><!-- painel opcional --></div>
  </div>
  <script>
    /* 1. Constantes e helpers
       2. AudioEngine (Web Audio API)
       3. Camera (opcional)
       4. Partículas
       5. Formas (drawStar, drawCoin, etc.)
       6. SCENES (array de cenas com init/draw)
       7. SCENE_CAPTIONS (legendas por cena)
       8. Sistema de legendas
       9. Transições
       10. Loop principal
       11. Gravação (MediaRecorder)
       12. Controles (play/pause/som/gravar) */
  </script>
</body>
</html>

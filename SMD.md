# postiz-smd

Postiz v2.25.1 (gitroomhq/postiz-app, AGPL-3.0) com uma alteração para a tela de post do TikTok atender às
diretrizes de UX do Direct Post (Safe Mode Dad / Core Labs):

- `creatorInfo` no provedor do TikTok (backend) devolve nome da conta, privacidades permitidas e bloqueios de
  comentário, duet e stitch, a partir de `/v2/post/publish/creator_info/query/`.
- A tela mostra "Posting to TikTok as ...", a privacidade começa sem valor e lista só as opções devolvidas,
  "Self only" some com Branded content, interações bloqueadas pela conta ficam desativadas e a confirmação de
  uso de música aparece sempre na publicação direta.
- DTO: privacidade obrigatória só em DIRECT_POST (UPLOAD continua igual); "Disclose" ligado exige Your brand
  ou Branded content.

Imagem: `ghcr.io/abreuedu/postiz-smd:<tag>`, gerada por `.github/workflows/image.yml` a cada tag `v*-smd.*`.

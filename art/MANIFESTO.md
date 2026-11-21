# Manifesto de assets — nomes exatos

Conferido contra `src/data/enemies.json`, `src/data/towers.json` e as cenas.
**Use exatamente estes nomes de arquivo** — o código vai procurar por eles.

Formato: **PNG com fundo transparente**. O Midjourney não gera transparência de
verdade: toda imagem desta lista (menos o terreno) precisa ser recortada depois.

Vista: **3/4 de cima (câmera 45°)**, luz do **topo-esquerda**, sombra fria.
Personagens e inimigos **virados para a direita** (o código espelha para a esquerda).

---

## inimigos/  — 8 arquivos

| Arquivo | Quem é | Observação |
|---|---|---|
| `goblin.png` | Goblin | o mais comum do jogo — pequeno, magro, corcunda, orelhas pontudas |
| `wolf.png` | Lobo de Guerra | quadrúpede, veloz |
| `grunt.png` | Orc Grunt | soldado orc padrão |
| `ogre.png` | Ogro | grande, pesado, lento |
| `gargoyle.png` | Gárgula | **voador** — pedra viva, asas de morcego |
| `wyvern.png` | Wyvern | **voador** — réptil alado, maior que a gárgula |
| `warlord.png` | Senhor da Guerra Orc | **chefe** das fases 1–3, imponente |
| `dragon.png` | O Dragão | **chefe final**, voador, o maior de todos |

Voadores precisam ler como voadores vistos de cima (asas abertas, corpo elevado).

## torres/ — 13 arquivos

Cada torre em 3 níveis. A **silhueta tem que mudar** entre níveis — o jogador
identifica o nível de relance, não lendo número.

| Torre | Arquivos |
|---|---|
| Arqueiros | `archer-1.png` `archer-2.png` `archer-3.png` |
| Arcana de Gelo | `ice-1.png` `ice-2.png` `ice-3.png` |
| Canhão Anão | `cannon-1.png` `cannon-2.png` `cannon-3.png` |
| Balista | `ballista-1.png` `ballista-2.png` `ballista-3.png` |
| Muralha | `wall.png` (nível único — barreira sem ataque) |

Todas assentadas num alicerce circular de pedra (é o que encaixa na grade de 40px).

## construcoes/ — 3 arquivos

| Arquivo | Quem é | Observação |
|---|---|---|
| `castelo.png` | Castelo do jogador | **um só**, sem níveis. Fica na borda direita |
| `portal.png` | Portal dos orcs | **um só**, sem níveis. Borda esquerda. O pulso é animado por código |
| `chefao.png` | Chefão de fase | fica ao lado do portal e avança a cada onda vencida |

## personagens/ — 4 arquivos

| Arquivo | Quem é |
|---|---|
| `heroi.png` | Herói (guerreiro) — fica junto ao castelo |
| `heroina.png` | Heroína (guerreira) — variante escolhida no menu |
| `principe.png` | Príncipe cativo — acorrentado, braços erguidos, expressão triste |
| `princesa.png` | Princesa cativa — mesma pose |

Os cativos aparecem na masmorra entre fases, presos por argolas nos pulsos.

## cenario/ — avulso, gere variações

Provavelmente o **maior ganho por esforço**: hoje as árvores são brócolis de
círculos e as pedras são bolinhas cinzas.

| Arquivo | Observação |
|---|---|
| `arvore-1.png` … `arvore-3.png` | 3 variações — o campo repete muito |
| `pedra-1.png` `pedra-2.png` | rochas de tamanhos diferentes |
| `arbusto-1.png` `arbusto-2.png` | vegetação baixa |

## (raiz) — terreno

| Arquivo | Estado |
|---|---|
| `field.jpg` | **já entregue.** Precisa do upscale (hoje é a grade 4-up) |

---

## NÃO gere — não existe no jogo

Orc Berserker · Orc Shaman · Torre de Mago · Torre de Veneno ·
Castelo níveis 1/2/3 · Portal níveis 1/2/3

---

## Regra de ouro: trave o estilo primeiro

Aprove **um** asset, guarde a URL dele e use `--sref <URL> --sw 100` em todos os
outros. Sem isso o resultado é um conjunto de imagens bonitas que não parecem do
mesmo jogo — e o retrabalho é total.

> **URL de referência de estilo:** _(preencher assim que aprovar a primeira)_

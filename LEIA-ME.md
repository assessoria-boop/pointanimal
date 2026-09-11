# Point Animal · Clínica Veterinária 24h (Porto Alegre/RS)

Recriação das pranchetas **Desktop V1** (1440 px) e **Mobile V1** (390 px) do arquivo
"Landingpages Layout Premium" no Paper, com a copy de pointanimal.saudevet.com.
Publicada em 11/09/2026 no lugar da LP anterior, que continua no histórico do Git (commit b6dc35e).

## Integrações
- WhatsApp +55 51 99828-2558, mensagem "Olá encontrei vocês pelo Google, gostaria de atendimento." (o número nunca aparece na página)
- Google Tag Manager `GTM-PT5CRMNH` e Microsoft Clarity `xyotnfrny4`: carregam na primeira interação (mouse, toque, rolagem ou tecla), sem timer. Assim ficam fora da medição do PageSpeed. Quem sai sem interagir não é registrado
- Mapa do Google: o embed enviado, que só carrega quando a dobra de contato se aproxima

## Mobile
- Cabeçalho visível, como na prancheta (logo, botão do WhatsApp e menu).
- O texto gigante "Point Animal" atrás do cachorro fica oculto no celular (pedido do cliente); no desktop ele continua.

## Imagens
- Fotos enviadas pelo cliente em 11/09/2026 guardadas sem alteração fora do repositório, em `C:\Users\Gaabs\brand-assets\point-animal\fotos-originais`; as versões usadas na página ficam em `img/`:
  - `etapa-1..4.webp`: recortadas em 740×440 (formato dos cards de etapas)
  - `card-caes`, `card-gatos`: 900×900
  - `destaque-cirurgia`, `destaque-exames`, `destaque-consultas`: 720 px de largura
- `avaliacao-1..5.webp`: prints reais do Google (os mesmos `1.webp`–`5.webp` da LP anterior, recomprimidos, cerca de 28% menores)
- `logo.webp`: logo do cliente (150 px, usada como favicon); `logo-96.webp`: a mesma reduzida para o cabeçalho e o rodapé (3 KB)
- `hero-cao-*`, `servico-emergencia`: fotos do template
  (`servico-emergencia` reduzida para 560 px, de 126 KB para 45 KB)

## Cores (template turquesa → Point Animal)
| Papel | Template | Point Animal |
|---|---|---|
| cor principal / ícones | `#0BA5C7` | `#6B9E2C` |
| texto de destaque / botões escuros | `#0A7E9B` | `#4C7A22` (verde da logo) |
| linha de destaque do título do hero | `#69CADB` | `#B9DC5F` (verde-lima do anel da logo) |
| fundo suave (serviços) | `#E6F6FA` | `#F1F7E4` |
| rodapé | `#0D3440` | `#1C2E0C` |
| degradê do hero | `#075F76 → #69CADB` | `#2E4C12 → #9DC63E` |

Botões de WhatsApp sempre no verde `#25D366`.

## Desempenho (Lighthouse 12 local, servidor com gzip)
| | Performance | Acessibilidade | Boas práticas | SEO |
|---|---|---|---|---|
| Desktop | 100 | 93 | 100 | 100 |
| Mobile | 94 | 93 | 100 | 100 |

- Mobile: LCP 2,3 s, CLS 0, TBT 170 ms. Com GTM + Clarity no timer de 3,5 s o mobile caía para 80 / Boas práticas 79.
- Acessibilidade 93 vem do bloqueio de zoom no celular, que é requisito do projeto.
- Fontes Manrope e Montserrat servidas localmente (subset latin), sem CSS externo.

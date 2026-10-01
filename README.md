# Trama Store

Site de uma loja de roupas fictícia, feito para a atividade da **Aula 7 de Web Design: Box Model e Flexbox**.

**Facens · Prof. Deivison S. Takatu**

A Trama Store é uma loja pequena com oito peças básicas em tecidos naturais. O site tem estas seções:

- barra de aviso
- cabeçalho com menu
- banner
- categorias
- vitrine de produtos
- destaque da coleção
- vantagens
- sobre a loja
- depoimentos
- newsletter
- contato
- rodapé

O projeto usa só **HTML e CSS**:

- **Arquivos:** um `index.html` e um `style.css`, ligado pela tag `<link>`.
- **Sem estilo inline:** não há `style=""` nem `<style>` no HTML.
- **Sem dependências:** não há JavaScript, frameworks nem bibliotecas. Só as fontes vêm do Google Fonts.
- **Comentários:** todo o código está comentado em português.
- **Marcações no CSS:** cada elemento de Box Model e cada uso de Flexbox está marcado com `BOX MODEL NN` ou `FLEX NN`.

## Integrantes

| Integrante |
|---|
| Gabriel Martins Antunes |
| Gabriel Martins Antunes |
| Vitor Hugo Rosario do Santos |
| Matheus Giachetti |

São dois alunos diferentes com o nome Gabriel Martins Antunes.

## Como abrir o site

1. Baixe o projeto. Você pode clonar o repositório:
   ```bash
   git clone https://github.com/matheusgiachetti/aula07-flexbox-loja.git
   ```
   Ou, no GitHub, clicar em **Code > Download ZIP** e extrair o arquivo.
2. Abra o arquivo `index.html` em qualquer navegador (Chrome, Edge ou Firefox). Não é preciso instalar nada nem rodar servidor.
3. Para ver a versão de celular e de tablet, diminua a largura da janela. Outra opção é apertar `F12` e ativar o modo de dispositivo (`Ctrl + Shift + M`).

## Estrutura dos arquivos

```
aula07-flexbox-loja/
├── index.html     estrutura da página (862 linhas)
├── style.css      todo o visual do site (2188 linhas)
├── imagens/       8 fotos dos produtos (Unsplash)
├── .gitignore
└── README.md
```

O `style.css` está dividido nesta ordem:

1. variáveis de cor, fonte e espaçamento;
2. reset;
3. estilos de cada seção, na mesma ordem em que elas aparecem na página;
4. efeitos de hover;
5. media queries;
6. no fim, um comentário com o resumo de Box Model e Flexbox.

## Responsividade

| Largura da tela | O que muda |
|---|---|
| até 1024px | A vitrine passa de 4 para 2 cards por linha. |
| até 900px (tablet) | O menu desce para uma segunda linha. O destaque vira coluna, com a foto em cima. |
| até 600px (celular) | O menu, o banner, o destaque e o rodapé ficam em coluna (`flex-direction: column`). A vitrine mostra 1 card por linha, com a largura toda. |

Cards e botões têm efeitos de hover com `transition`, `transform` e `box-shadow`. Os mesmos efeitos aparecem com o teclado (`:focus-visible`). Se o sistema estiver configurado para reduzir animações, os movimentos são desligados.

## Box Model: 20 elementos

Cada elemento tem valores definidos de **conteúdo** (width/height ou max-width/min-height), **padding**, **border** e **margin**. No `style.css`, cada um está marcado com `BOX MODEL NN` logo acima da regra.

| Nº | Elemento | Conteúdo | Padding | Border | Margin |
|---|---|---|---|---|---|
| 01 | `.cabecalho-conteudo` | width 100%, max-width 1200px, height 72px | 0 24px | border-bottom 1px | 0 auto |
| 02 | `.logo` | height 40px | 4px 12px | 1.5px | margin-right 16px |
| 03 | `.menu-link` | height 40px | 0 2px | border-bottom 2px (aparece no hover) | 0 4px |
| 04 | `.sacola` | height 40px | 0 16px | 1px | margin-left 8px |
| 05 | `.sacola-contador` | 22px × 22px | 2px | 1px | margin-left 2px |
| 06 | `.hero` | width 100%, min-height 560px | 80px 24px | border-bottom 1px | margin-bottom 48px |
| 07 | `.hero-conteudo` | width 100%, max-width 1200px | 8px 0 8px 48px | border-left 2px | 0 auto |
| 08 | `.hero-selo` | height 28px | 0 16px | 1px | margin-bottom 4px |
| 09 | `.botao` | min-width 180px, height 52px | 0 28px | 1px | margin-top 8px |
| 10 | `.secao-cabecalho` | width 100% | padding-bottom 24px | border-bottom 1px | margin-bottom 48px |
| 11 | `.categoria-card` | width 100%, min-height 220px | 24px | 1px | margin-bottom 4px |
| 12 | `.categoria-numero` | 36px × 36px | 4px | 1px | margin-bottom 16px |
| 13 | `.produto` | min-width 200px | 8px | 1px | margin-bottom 8px |
| 14 | `.produto-selo` | height 26px | 0 10px | 1px | 8px |
| 15 | `.tamanho` | min-width 34px, height 30px | 0 6px | 1px | 0 (o espaço vem do `gap`) |
| 16 | `.botao-sacola` | width 100%, height 44px | 0 16px | 1px | margin-top auto |
| 17 | `.barra-aviso` | width 100%, height 36px | 0 16px | border-bottom 2px | 0 (encosta no topo) |
| 18 | `.destaque-ficha` | width 100%, max-width 480px | 8px 24px | 1px | 8px 0 |
| 19 | `.destaque-imagem` | height 600px | 12px | 1px | margin-right 80px |
| 20 | `.destaque-legenda` | height 34px | 0 16px | 1px | 24px |

Outros 12 elementos também têm o Box Model completo e estão marcados de 21 a 32:

- `.vantagens-lista`
- `.vantagem-icone`
- `.depoimento`
- `.depoimento-produto`
- `.depoimento-avatar`
- `.sobre-numeros`
- `.newsletter-caixa`
- `.newsletter-campo`
- `.newsletter-botao`
- `.contato-item`
- `.rodape`
- `.integrante`

## Flexbox: 20 usos

Cada uso é uma propriedade com valor e tem efeito visível na página. No `style.css`, cada um está marcado com `FLEX NN`. No total, o arquivo tem 73 marcações FLEX.

| Marcação | Propriedade e valor | Elemento | O que acontece na tela |
|---|---|---|---|
| FLEX 01 | `display: flex` | `.cabecalho-conteudo` | Logo, menu e sacola ficam na mesma linha. |
| FLEX 01 | `justify-content: space-between` | `.cabecalho-conteudo` | Logo fica na esquerda e sacola na direita. |
| FLEX 01 | `align-items: center` | `.cabecalho-conteudo` | Os três blocos ficam centralizados na altura. |
| FLEX 03 | `gap: 24px` | `.menu-lista` | Espaço igual entre os links do menu. |
| FLEX 08 | `flex-direction: column` | `.hero-conteudo` | Selo, título, texto e botões do banner ficam empilhados. |
| FLEX 19 | `flex-wrap: wrap` | `.vitrine-grade` | Os cards descem de linha quando não cabem. |
| FLEX 20 | `flex-basis: calc(25% - 18px)` | `.produto` | 4 cards por linha no computador. |
| FLEX 22 | `flex-grow: 1` | `.produto-info` | Os botões de todos os cards ficam alinhados embaixo. |
| FLEX 28 | `flex-direction: row-reverse` | `.destaque` | A foto fica à esquerda, mesmo vindo depois no HTML. |
| FLEX 31 | `display: inline-flex` | `.etiqueta` | A etiqueta fica do tamanho do texto. |
| FLEX 38 | `flex: 1 1 220px` | `.vantagem` | As quatro vantagens dividem a linha por igual. |
| FLEX 39 | `flex-shrink: 0` | `.vantagem-icone` | O texto não espreme o ícone. |
| FLEX 44 | `align-self: flex-start` | `.depoimento-produto` | A etiqueta não estica na largura do card. |
| FLEX 50 | `flex: 2 1 400px` | `.sobre-texto` | A coluna de texto cresce o dobro da coluna do título. |
| FLEX 61 | `flex-flow: row wrap` | `.rodape-colunas` | As colunas do rodapé ficam lado a lado, com `column-gap` e `row-gap` diferentes. |
| FLEX 69 | `order: 3` | `.menu` (tablet) | O menu vai para a linha de baixo do cabeçalho. |
| FLEX 70 | `order: -1` | `.destaque-imagem` (tablet e celular) | A foto fica acima do texto. |
| FLEX 71 | `align-content: flex-start` | `.menu-lista` (celular) | As duas colunas de links ficam juntas à esquerda. |
| FLEX 72 | `flex-direction: column` | `.hero-botoes` (celular) | Os botões do banner ficam um embaixo do outro. |
| FLEX 73 | `flex-flow: column nowrap` | `.rodape-colunas` (celular) | O rodapé fica empilhado em coluna. |

Onde aparece cada propriedade exigida pela atividade:

| Propriedade | Marcação |
|---|---|
| `display: flex` | 01 |
| `display: inline-flex` | 31 |
| `flex-direction` | 08, 28 e 72 |
| `flex-wrap` | 19 |
| `flex-flow` | 61 e 73 |
| `justify-content` | 01 |
| `align-items` | 01 |
| `align-content` | 71 |
| `align-self` | 44 |
| `order` | 69 e 70 |
| `flex-grow` | 22 |
| `flex-shrink` | 39 |
| `flex-basis` | 20 |
| `flex` | 38 e 50 |
| `gap` | 03 |

## Créditos das fotos

Todas as fotos são do [Unsplash](https://unsplash.com) e usam a [licença gratuita do Unsplash](https://unsplash.com/license). Elas foram baixadas em 800px de largura para o site carregar rápido.

| Arquivo | Peça | Autor | Link da foto |
|---|---|---|---|
| `camiseta-basica.jpg` | Camiseta Básica | Avtar Singh | https://unsplash.com/photos/8ACmRoleM24 |
| `camiseta-listrada.jpg` | Camiseta Listrada | Matthieu Jungfer | https://unsplash.com/photos/eGz4OMdCmYM |
| `calca-reta-sarja.jpg` | Calça Reta de Sarja | saeed karimi | https://unsplash.com/photos/lBi04ECUJfw |
| `calca-pantalona-linho.jpg` | Calça Pantalona de Linho | Kurt Liwanag | https://unsplash.com/photos/AHunEsfCpxk |
| `jaqueta-jeans.jpg` | Jaqueta Jeans Clássica | Adrian Dascal | https://unsplash.com/photos/1QOsJGbNIgk |
| `vestido-midi-linho.jpg` | Vestido Midi de Linho | Lance Reis | https://unsplash.com/photos/hElEUd24xQo |
| `vestido-chemise.jpg` | Vestido Chemise Listrado | Laura Chouette | https://unsplash.com/photos/b7SROo2EXG8 |
| `bolsa-tote-lona.jpg` | Bolsa Tote de Lona | Brando Makes Branding | https://unsplash.com/photos/smTDI-z1rlY |

A foto do vestido midi também aparece na seção de destaque da coleção.

## Observação

A Trama Store é uma loja **fictícia**, criada só para fins acadêmicos. São inventados:

- o endereço, os telefones, o e-mail e os perfis de redes sociais;
- os depoimentos;
- as informações sobre a oficina.

O formulário de newsletter e os botões "Adicionar à sacola" são só visuais e não enviam nada.

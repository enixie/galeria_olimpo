### Olimpo Gallery - Exemplo de Galeria com Lightbox

Este projeto demonstra uma galeria de imagens simples com funcionalidade de lightbox, implementada utilizando HTML, CSS e JavaScript puro. Abaixo está uma explicação e aprendizados principais do código:

#### Estrutura HTML (`index.html`)

O arquivo HTML define a estrutura básica da página web. Elementos principais incluem:
- **Tags `<meta>`**: Define o conjunto de caracteres e viewport para responsividade.
- **`<link>`**: Referencia uma folha de estilo externa (`style.css`) para estilização.
- **`<script>`**: Referencia um arquivo JavaScript externo (`script.js`).
- **Div `.grid`**: Contém um layout de grid (`display: grid`) para exibição das imagens.
- **Imagens**: Cada tag `<img>` dentro de `.grid` referencia um arquivo de imagem (diretório `img/`) com atributos `alt` para acessibilidade.

#### JavaScript (`script.js`)

JavaScript melhora a galeria com funcionalidades interativas:
- **Criação Dinâmica do Lightbox**:
  - Cria um `<div>` (`lightbox`) dinamicamente quando uma imagem é clicada.
  - Adiciona um `id` e o anexa ao `<body>`.
- **Ouvintes de Evento**:
  - Adiciona um ouvinte de evento de clique a cada imagem (`<img>`).
  - Quando clicada, adiciona a classe `active` ao `lightbox` para exibi-lo.
  - Clona a imagem clicada dentro do `lightbox` para visualização detalhada.
- **Fechamento do Lightbox**:
  - Adiciona um ouvinte de evento de clique ao `lightbox` em si.
  - Quando clicado (não na imagem), remove a classe `active` para ocultar o `lightbox`.

#### CSS (`style.css`)

As folhas de estilo CSS definem a apresentação visual:
- **Layout de Grid**:
  - Utiliza CSS Grid (`display: grid`) para um layout responsivo de imagens, distribuídas uniformemente (`200px` cada, três por linha).
- **Estilização de Imagens**:
  - Define dimensões fixas (`width` e `height`) para uniformidade.
  - Aplica `cursor: pointer` para indicar interatividade.
- **Estilização do Lightbox**:
  - Posicionado `fixed` para sobrepor a tela inteira.
  - Inicialmente oculto (`display: none`)

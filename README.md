# 🚲 Bikcraft

Site institucional e de vendas da **Bikcraft**, uma loja fictícia de bicicletas elétricas feitas sob medida. O projeto foi desenvolvido como conclusão do curso de **HTML5 e CSS3** e coloca em prática layout responsivo, CSS modular, formulários e acessibilidade, **sem JavaScript**.

## 📄 Páginas

| Página | Arquivo | Descrição |
| --- | --- | --- |
| Home | `index.html` | Apresentação, lista de bicicletas, tecnologia, parceiros, depoimento e planos de seguro |
| Bicicletas | `bicicletas.html` | Catálogo com os três modelos e suas características |
| Detalhe da bicicleta | `bicicletas/magic.html`, `nimbus.html`, `nebula.html` | Galeria de fotos, preço, entrega, estoque e informações técnicas |
| Seguros | `seguros.html` | Planos Prata e Ouro, vantagens e perguntas frequentes |
| Contato | `contatos.html` | Formulário de contato, dados da loja online e lojas físicas (RJ e SP) |
| Orçamento | `orcamentos.html` | Formulário de orçamento de bicicleta ou seguro |
| Termos | `termos.html` | Termos e condições de uso |

### Modelos

| Modelo | Preço |
| --- | --- |
| Magic Might | R$ 2.499 |
| Nebula Cosmic | R$ 3.999 |
| Nimbus Stark | R$ 4.999 |

### Seguros

| Plano | Preço |
| --- | --- |
| Prata | R$ 199/mês |
| Ouro | R$ 299/mês |

## 🛠️ Tecnologias e técnicas

- **HTML5** semântico: `header`, `nav`, `main`, `article`, `section`, `address`, `blockquote`, `dl`, `picture` e outros
- **CSS3** puro, com:
  - **Custom properties** (`var(--c0)`, `var(--p1)`) para a paleta de cores
  - **CSS Grid** e **Flexbox** nos layouts
  - **Media queries** (`1200px`, `800px`, `600px` e `400px`) para o design responsivo
  - **Imagens responsivas** com `<picture>` e `<source media>`
  - **Pseudo-elementos** (`::before`, `::after`) em decorações, sublinhados animados e ícones
  - **Transições** nos links, menu e botões
  - **Formulário de orçamento sem JavaScript**: ele usa `input[type="radio"]` com `:checked` e o seletor `~` para alternar entre bicicleta e seguro e mostrar os detalhes do modelo escolhido
- **Google Fonts**: Poppins e Roboto (Merriweather também é carregada)
- **SVG** para logo, ícones, redes sociais, parceiros e decorações
- **Git** para o versionamento

## 🗂️ Estrutura

```
projeto-bikcraft/
├── index.html
├── bicicletas.html
├── seguros.html
├── contatos.html
├── orcamentos.html
├── termos.html
├── bicicletas/
│   ├── magic.html
│   ├── nebula.html
│   └── nimbus.html
├── css/
│   ├── style.css            # importa todos os outros arquivos CSS
│   ├── global/              # header, footer e reset
│   ├── utils/               # cores, tipografia, componentes e formulário
│   ├── home/                # introdução, tecnologia, parceiros e depoimento
│   ├── bicicletas/          # lista e catálogo de bicicletas
│   ├── bicicleta/           # página de cada modelo
│   ├── seguros/             # seguros, vantagens e perguntas frequentes
│   ├── contato/             # contato e lojas
│   ├── orcamento/           # formulário de orçamento
│   └── termos/
└── img/
    ├── bicicletas/ bicicleta/ fotos/ lojas/   # fotos (.jpg)
    └── icones/ redes/ parceiros/ dec/         # SVGs
```

### Organização do CSS

O CSS é dividido por página e por função. O `css/style.css` reúne tudo com `@import`, e cada página carrega só esse arquivo. Nas pastas `utils/`, os estilos reutilizáveis ficam em classes pequenas:

- `.container`: largura máxima de 1200px, centralizado
- `.botao`, `.botao.secundario`, `.botao.seta` e `.link`: botões e links de destaque
- `.font-1-*` (Poppins) e `.font-2-*` (Roboto): escala tipográfica (`xs` a `xxl`)
- `.c0`–`.c12` (tons de cinza) e `.p1`–`.p5` (amarelo da marca): cores

## 🚀 Como executar

O projeto é estático e não precisa de instalação nem de build.

```bash
git clone git@github.com:luishen-r/projeto-Bikcraft.git
cd projeto-Bikcraft
```

Abra o `index.html` no navegador. Se preferir um servidor local, use a extensão **Live Server** do VS Code ou rode `python3 -m http.server`. Precisa de internet para carregar as fontes do Google Fonts.

## 📚 Aprendizados

- Estruturar o CSS em módulos reutilizáveis
- Construir layouts responsivos com Grid e Flexbox
- Interações só com CSS (`:checked`, `:hover`, `:focus`)
- Usar HTML semântico e pensar em acessibilidade
- Organizar o projeto com Git

## 👤 Autor

**Luis Henrique**
GitHub: [@luishen-r](https://github.com/luishen-r)

---

> Projeto com fins educacionais. A marca, os produtos e os contatos da Bikcraft são fictícios.

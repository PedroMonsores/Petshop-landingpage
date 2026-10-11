# 🐾 Do Pet Au Vet — Site Institucional

Site institucional da **Do Pet Au Vet** — clínica veterinária e petshop localizada na Jatiúca, Maceió. Apresenta serviços, loja de produtos, avaliações de clientes e canais de contato.

---

## 📁 Estrutura do projeto

```
do-pet-au-vet/
├── index.html              Home (hero + destaques + reviews + FAQ + CTA)
├── servicos.html           Página de serviços (6 categorias)
├── loja.html               Loja de produtos (8 itens — sem checkout)
├── README.md               Este arquivo
│
├── 📁 css/
│   └── styles.css          Animações customizadas (floaty, scroll)
│
└── 📁 images/
    ├── hero-image.jpg      Foto principal do topo (800×1000)
    ├── og-image.jpg        Preview social (1200×630)
    └── 📁 products/
        ├── product-1.jpg   Ração Salmão & Proteína
        ├── product-2.jpg   Osso de Borracha
        ├── product-3.jpg   Cama Ortopédica
        ├── product-4.jpg   Shampoo de Aveia
        ├── product-5.jpg   Ração Natural Filhotes
        ├── product-6.jpg   Coleira Antipulgas
        ├── product-7.jpg   Varinha Interativa para Gatos
        └── product-8.jpg   Tapete Higiênico
```

---

## 🚀 Como rodar o projeto

### Opção 1 — Duplo clique (mais simples)
Abra `index.html` direto no navegador.

> ⚠️ Alguns recursos podem não funcionar em `file://`. Prefira a Opção 2.

### Opção 2 — Live Server (recomendado)

**Com VS Code:**
1. Instale a extensão **Live Server** de Ritwick Dey
2. Clique com o botão direito em `index.html` → **Open with Live Server**
3. O site abrirá em `http://127.0.0.1:5500`

**Com Python (já vem instalado no Mac/Linux):**
```bash
cd do-pet-au-vet
python3 -m http.server 8000
```
Depois abra `http://localhost:8000` no navegador.

**Com Node.js:**
```bash
npx serve do-pet-au-vet
```

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Uso |
|---|---|
| **HTML5** | Estrutura semântica das 3 páginas |
| **Tailwind CSS (CDN)** | Estilização via classes utilitárias |
| **JavaScript (vanilla)** | Menu mobile + interações |
| **Google Fonts** | Tipografia: *Baloo 2* (títulos) + *Plus Jakarta Sans* (corpo) |
| **SVG inline** | Ícones, favicon e logo |

**Sem build, sem dependências.** Nenhum `npm install` é necessário para desenvolvimento ou produção.

---

## 🎨 Paleta de cores

Definida no `tailwind.config` de cada página:

| Nome | Uso | Exemplo |
|---|---|---|
| **`plum`** (roxo ameixa) | Cor primária — header, CTAs, destaques | `#6A2B58` |
| **`brand`** (azul claro) | Cor secundária — ícones, badges, detalhes | `#39A5CA` |
| **`ink`** (preto quase puro) | Textos e superfícies escuras (footer) | `#0A0A0C` |
| **`cream`** | Fundo geral das páginas | `#FBFCFE` |

### Regras visuais do projeto
- **Texto** sempre em `text-ink` (preto)
- **Superfícies escuras** sempre em `bg-ink` (footer, faixa CTA final)
- **Botões primários** sempre em `bg-plum-600` (roxo)
- **Botões secundários** brancos com borda
- **Hover** de links em `text-brand-300` / `text-brand-500` (azul)

---

## 📄 Páginas

### `index.html` — Home
1. **Header** fixo (roxo plum) com Instagram, WhatsApp, telefone e CTA
2. **Hero** — foto principal + 2 CTAs + prova social (4.9/5)
3. **Trust bar** — 4 números (12+ anos, 2.000+ tutores, 30+ marcas, 24/7)
4. **Destaque duplo** — 2 cards grandes: Serviços (roxo) e Loja (azul)
5. **Reviews** compactos — 3 avaliações com avatar
6. **FAQ** — 5 perguntas com `<details>`
7. **CTA final** — faixa escura com desconto de primeira visita
8. **Footer** em 4 colunas

### `servicos.html` — Serviços
- Hero com breadcrumb
- 6 cards de serviço com ícones e preço "a partir de"
- CTA final
- Anchors para deep-link: `#banho`, `#veter`, `#daycare`, `#training`, `#taxi`

### `loja.html` — Loja
- Hero com breadcrumb + 3 selos
- Grid de 8 produtos (nome + descrição + preço, **sem botão de compra**)
- Aviso "preços de amostra"
- CTA final

---

## 🔧 Como customizar

### 📸 Trocar as imagens

Substitua os arquivos mantendo **os mesmos nomes**:

| Arquivo | Tamanho ideal | Proporção |
|---|---|---|
| `images/hero-image.jpg` | 800 × 1000 px | 4:5 (retrato) |
| `images/og-image.jpg` | 1200 × 630 px | 1.91:1 |
| `images/products/product-1.jpg` … `product-8.jpg` | 800 × 800 px | 1:1 (quadrado) |

- **Formato:** JPG ou WebP (WebP é ~40% mais leve)
- **Peso máximo:** ~150 KB por arquivo ([TinyPNG](https://tinypng.com) ou [Squoosh](https://squoosh.app))
- **Nomes:** sempre minúsculos, com hífen, sem acentos (ex.: `product-1.jpg`, não `Product 1.jpg`)

### 🔗 Trocar links de contato

Busque e substitua nos 3 arquivos HTML:

| Placeholder atual | Substitua por |
|---|---|
| `https://instagram.com/dopetauvet` | URL real do Instagram |
| `https://wa.me/5551234567` | `https://wa.me/55DDDNUMERO` (só dígitos) |
| `tel:+15551234567` | `tel:+55DDDNUMERO` |
| `email@dopetauvet.com` | E-mail real |
| `Rua Estudante Carlos Moura Gama, 123, Jatiúca` | Endereço real |

### 📬 Ativar a newsletter (Formspree)

1. Crie conta em [formspree.io](https://formspree.io)
2. Crie um novo formulário → copie o ID (ex.: `xyzabcd`)
3. Nos 3 arquivos HTML, substitua `SEU_ID`:
   ```html
   <form action="https://formspree.io/f/xyzabcd" method="POST">
   ```

### 📝 Editar textos

- **Títulos, subtítulos, descrições** — edite direto no HTML (os textos estão legíveis, sem minificação)
- **Menu de navegação** — em cada página, no bloco `<nav>` do header
- **Redes sociais** — header, menu mobile e footer (3 lugares por página)

---

## ✅ Boas práticas aplicadas

- **Acessibilidade** — `aria-label` nos botões de ícone, `alt` em imagens, `sr-only` em textos visuais alternativos, contraste adequado
- **SEO básico** — `<title>`, `<meta description>` e Open Graph (preview ao compartilhar no WhatsApp/Instagram)
- **Performance** — `loading="lazy"` nas imagens de produto, SVGs inline, Tailwind CDN
- **Responsivo** — 3 breakpoints (mobile / `sm` / `lg`)
- **Sem dependências de build** — funciona abrindo direto no navegador

---

## 🐛 Problemas comuns

| Problema | Solução |
|---|---|
| Imagem não aparece | Verifique nome (minúsculo, hífen), extensão (`.jpg`) e caminho (`images/...`) |
| Menu mobile não abre | Confirme que o `<script>` no fim do `<body>` está presente |
| Header/footer desconfigurado | Não remova as classes `grid`, `lg:grid-cols-*` e `lg:flex` |
| Newsletter não envia | Troque `SEU_ID` pelo ID real do Formspree |

---

## 🚀 Deploy

Este é um site **estático** — funciona em qualquer hospedagem:

| Serviço | Custo | Como fazer |
|---|---|---|
| **Netlify** | Grátis | Arraste a pasta em [app.netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | Grátis | `vercel` na raiz do projeto |
| **GitHub Pages** | Grátis | Suba para um repo e ative Pages nas configurações |
| **Cloudflare Pages** | Grátis | Conecte o repositório GitHub |
| **Hostinger / HostGator** | Pago | Suba os arquivos via FTP para a pasta `public_html` |

**Domínio próprio:** compre em [Registro.br](https://registro.br) (~R$ 40/ano para `.com.br`) ou em registradores internacionais (~US$ 10/ano para `.com`).

---

## 📈 Melhorias futuras sugeridas

- [ ] Migrar do Tailwind CDN para build local (reduz ~300 KB)
- [ ] Adicionar Google Analytics ou Plausible (métricas de visita)
- [ ] Integrar com Google Meu Negócio (aparecer no mapa)
- [ ] Botão flutuante de WhatsApp (fixo no canto inferior direito)
- [ ] Blog com dicas de cuidado animal (SEO + autoridade)
- [ ] Sistema de agendamento online (Calendly, Cal.com)
- [ ] Versão em inglês (para turistas em Maceió)

---

## 📄 Licença

Projeto proprietário da **Do Pet Au Vet**. Todos os direitos reservados.

Última atualização: **2026**

---

## 📞 Contato

- 📷 Instagram: [@dopetauvet](https://instagram.com/dopetauvet)
- 💬 WhatsApp: [(555) 123-4567](https://wa.me/5551234567)
- 📧 E-mail: email@dopetauvet.com
- 📍 Endereço: Rua Estudante Carlos Moura Gama, 123 — Jatiúca, Maceió/AL

# 📄 ResumeGen Pro

Um gerador de currículos profissional, interativo e de alto desempenho construído inteiramente em um **único arquivo** (HTML/CSS/JS). Ideal para quem precisa criar um currículo atraente, com exportação rápida para PDF sem precisar enviar dados para servidores externos.

## ✨ Funcionalidades

- ⚡ **Single File Architecture:** Toda a aplicação vive em um único arquivo `index.html`. Não requer build, Node.js ou dependências locais para rodar.
- 🎨 **Templates Dinâmicos:**
  - **Moderno:** Layout assimétrico em duas colunas, tipografia Sans-Serif e cores de destaque. Ideal para vagas de tecnologia e criatividade.
  - **Clássico:** Layout de coluna única, tipografia Serifada e separadores elegantes. Ideal para ambientes formais e corporativos.
- 💾 **Auto-Save:** Não perca seu progresso! Todas as alterações são salvas automaticamente no `localStorage` do seu navegador assim que você digita.
- 👁️ **Preview em Tempo Real:** Um papel virtual A4 exibe as alterações instantaneamente, mantendo a escala inteligente de acordo com o tamanho da sua tela.
- 🏷️ **Tags Inteligentes:** Adicione habilidades pressionando a tecla `Enter`.
- ➕ **Sessões Dinâmicas:** Adicione ou remova blocos de Experiência Profissional e Formação Acadêmica de forma infinita.
- 📥 **Exportação para PDF:** Geração de PDF em alta resolução client-side, utilizando `jsPDF` e `html2canvas` mantendo máxima fidelidade visual.

## 🚀 Como Usar

### Pré-requisitos
Você só precisa de um navegador web moderno (Chrome, Firefox, Edge, Safari). Nenhuma instalação é necessária.

### Rodando o Projeto
1. **Método Local Direto:** Dê um duplo-clique no arquivo `index.html` para abri-lo no seu navegador.
2. **Servidor HTTP (Recomendado para evitar bloqueios de CORS por fontes externas):** 
   Se você tiver o Node.js instalado, abra o terminal na pasta do projeto e rode:
   ```bash
   npx http-server . -p 8080
   ```
   Acesse: `http://localhost:8080`

### Fluxo de Uso
1. **Preencha seus Dados:** O lado esquerdo da tela contém o formulário. Preencha suas informações de contato, anexe uma foto de perfil e preencha as experiências.
2. **Acompanhe o Preview:** O lado direito atualizará a identidade visual em tempo real.
3. **Escolha o Tema:** No cabeçalho superior, alterne entre "Clássico" e "Moderno" para mudar a aparência instantaneamente.
4. **Exporte:** Clique no botão azul "Baixar Currículo". Um arquivo PDF será processado e salvo na sua máquina com o seu nome.

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Estrutura semântica.
- **CSS3 Vanilla:** 
  - CSS Variables (Design Tokens) para manipulação instantânea de temas.
  - Layout Responsivo (CSS Grid e Flexbox).
  - Animações (`@keyframes`) e validações nativas (`:invalid`).
- **JavaScript Vanilla:** Lógica de manipulação reativa do DOM, `localStorage` e leitura assíncrona de imagem (`FileReader`).
- **Dependências Externas (via CDN):**
  - [jsPDF](https://github.com/parallax/jsPDF) e [html2canvas](https://html2canvas.hertzen.com/): Motor de captura e empacotamento do PDF.
  - [FontAwesome](https://fontawesome.com/): Biblioteca de ícones.
  - [Google Fonts](https://fonts.google.com/): Tipografias *Inter* e *Merriweather*.

## 💡 Arquitetura de Conversão (HTML -> PDF)

A geração do PDF neutraliza temporariamente o comportamento responsivo (zoom out/escala CSS) e força a renderização do elemento em pixels absolutos (`794px x 1123px` - equivalente A4 a 96DPI). O `html2canvas` captura essa área aplicando `scale: 2` (para dobrar a nitidez do vetor rasterizado) e o exporta como uma imagem JPEG de alta qualidade para dentro do documento gerenciado pelo `jsPDF`.

---
Desenvolvido com o foco em UX e modernidade na stack "Vanilla".

### RAW FOODSTORE — Pacote da Identidade Visual

Este repositório e pasta contêm os arquivos oficiais, especificações técnicas e diretrizes de aplicação da identidade visual da **Raw Foodstore**. 

### 🎨 Paleta de Cores

CorHexadecimalElemento / Aplicação
**🟡 **Amarelo****
#FFDD00Destaques principais e faixas
**⚫ **Preto****
#000000Elementos de contraste e tipografia
**⚪ **Papel****
#ECEAE7Fundos texturizados ou off-white
**🪙 **Cinza****
#EBEBEBFundos secundários e blocos
**🔲 **Borda****
#6A6A6ADelimitação de componentes e linhas

### 📐 Tipografia (Google Fonts)

* **Anton:** Utilizada em títulos, menus e chamadas principais. (Gratuita)
* **Inter:** Utilizada para blocos de textos longos, parágrafos e descrições. (Gratuita)

### 🛡️ Margens e Zona Segura

As regras abaixo são aplicadas rigidamente em todos os arquivos de prévia para garantir consistência visual em múltiplos dispositivos: 

* **Margens Externas:** 64 px em todos os lados (representada pela linha **magenta** nas guias).
* **Zona Central Quadrada:** 640 px (representada pela linha **ciano** nas guias). Todo conteúdo crítico (logo, título, subtítulo e etiquetas) deve ficar estritamente dentro desta área. 

  * *Motivo:* O preview do GitHub em configurações mobile adota a proporção **5:4** (cortando as laterais do padrão 2:1), enquanto o WhatsApp e outras redes cortam em **1:1**. Centralizando a composição, nada importante é perdido.
* **Faixa Inferior:** A faixa amarela cruza a imagem de ponta a ponta (composição de fundo), mas o seu texto correspondente deve se manter concentrado na zona central.
* **Logos (PNG/SVG):** O caractere R foi projetado para ocupar até 85% do círculo central, impedindo cortes acidentais em avatares redondos (GitHub, LinkedIn, Instagram).

### Como conferir as guias:

As linhas guias podem ser verificadas nos arquivos previa-social-guia-margens.png e og-image-guia-margens.png. 

* **No PSD:** Ative a camada oculta Guia - margem 64 e zona central 640.
* **No SVG:** Remova o atributo display="none" do grupo guia.
* **No HTML:** Altere a classe .guia de display: none para display: block.

⚠️ **Regra de Ouro:** Nenhuma alteração pode mover elementos importantes (texto ou logotipos) para fora dos limites das linhas magenta e ciano. 

### 📂 Mapeamento de Arquivos

### Pasta: previa-social/

#### Imagens Prontas (Distribuição)

* previa-social-1280x640.png: Dimensão otimizada para o GitHub (Settings > General > Social preview).
* previa-social-guia-margens.png: Cópia de validação técnica contendo as linhas de marcação.
* og-image-1200x630.png / .jpg: Imagens para Open Graph (WhatsApp, LinkedIn, Facebook). 

  * *Código de implementação para o site:* 

html

<meta property="og:image" content="URL-COMPLETA/og-image-1200x630.png">

Use o código com cuidado.
* og-image-guia-margens.png: Cópia de validação técnica para Open Graph.

#### Arquivos de Criação (Editáveis)

* previa-social-camadas.psd: Arquivo em camadas para edição rasterizada (contém 8 camadas organizadas: *fundo, quadrado, R, título, subtítulo, etiquetas, faixa, texto da faixa* + *guia oculta*). Compatível com Photoshop, Photopea (grátis via browser), GIMP, Krita e Affinity. 

  * *Nota:* Os textos originais estão rasterizados (pixels). Para alterá-los, remova a camada correspondente e reescreva utilizando a fonte **Anton** ou utilize o vetor abaixo.
* previa-social-camadas.svg: Arquivo vetorial com textos reais e grupos nomeados. Compatível com Figma, Inkscape, Illustrator e Affinity. 

  * *Requisito:* Instale a fonte **Anton** localmente antes de manipular o arquivo. Caso ocorram pequenos desalinhamentos, reajuste o tamanho da fonte.
* previa-social-anton.html: Modelo estruturado em código utilizando a fonte web Anton nativa. Para exportar, abra o arquivo no Google Chrome, inspecione o elemento #previa e use a ferramenta de desenvolvedor Capture node screenshot para gerar um PNG exato.

### Pasta: logo/

* logo-R-amarelo.svg / -512.png: Quadrado amarelo com o caractere R em preto. Recomendado para avatares, perfis de redes sociais e cabeçalhos de documentação.
* logo-R-preto.svg / -512.png: Quadrado preto com o caractere R em amarelo. Configuração idêntica à utilizada no favicon.

### 📝 Observações Importantes

* **Tipografia nos Arquivos Estáticos:** Os textos presentes nas mídias .png, .psd e .jpg (OG) foram renderizados originalmente com uma fonte condensada similar à Anton por indisponibilidade técnica momentânea. Para obter o desenho exato e atualizado da identidade, priorize o uso dos arquivos .svg ou do template .html.
* **Limitações do GitHub:** A plataforma aceita arquivos nos formatos PNG, JPG ou GIF. O peso total do arquivo deve ser rigorosamente **menor que 1 MB** e a resolução sugerida é de 1280 x 640 px.
* **Compatibilidade de Redes Sociais:** WhatsApp e LinkedIn apresentam inconsistências ao ler metadados de imagens no formato WebP. Mantenha preferencialmente as extensões .png ou .jpg configuradas na tag og:image.
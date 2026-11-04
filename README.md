# Canal RC · Portfólio de Rhuan Camargo

Portfólio interativo em formato de **canal de streaming** (visual original, sem copiar nenhuma plataforma real). Projetos viram séries, skills viram gêneros, cursos viram "Continue assistindo" e certificados viram "Conquistas".

Projeto do **Checkpoint 6: Vibecoding** (landing page criada com IA, documentando o processo). Feito com ajuda do Claude.

- **Repositório:** [PREENCHER]
- **Deploy (Netlify):** [PREENCHER]

---

## Como ver o site

Abra o `index.html` no navegador. Não precisa instalar nada: é um arquivo único com HTML, CSS e JavaScript puro. As fontes (Plus Jakarta Sans e JetBrains Mono) vêm do Google Fonts, então é preciso internet para elas carregarem.

```
/
├── index.html   (o site inteiro: visual, estrutura e interações)
└── README.md    (este arquivo)
```

---

## Onde modificar cada coisa

Dentro do `index.html`, use **Ctrl+F** nos títulos `=====` (por exemplo, `===== Dados reais`).

| Quero mudar... | Onde fica | Como |
|---|---|---|
| Cores | CSS, bloco `Tokens` | Troque as variáveis `--co` (destaque azul gelo), `--mn` (menta), `--bg`, `--sf`, `--tx`, `--mu` |
| Fontes | `<head>` (link do Google Fonts) e CSS `Tokens` (`--sans`, `--mono`) | Troque o link e o nome da fonte |
| Texto do "Sobre mim" | HTML, `<section id="sobre">` | Edite o texto direto |
| Links das redes | HTML, `<section id="contato">` | Troque os `href` |
| **Projetos** | JS, lista `PR` | Copie uma linha, mude `id` (único), `n`, `d`, `tech`, `repo` e `dep` |
| **Link do deploy do CineLog** | JS, lista `PR`, campo `dep` do `cinelog` | Troque `[PREENCHER]` pela URL |
| **Progresso de um curso** | JS, lista `CT` | Mude o 3º número (0 a 100) |
| **Certificados** | JS, lista `CQ` | `[nome, instituição, data, link]`; link vazio `''` deixa o botão desabilitado |
| Skills | JS, lista `SK` | `[gênero, cor, [skills]]` |
| Seção "Em breve" | JS, lista `EB` | Troque os nomes e tire o `[PREENCHER]` do HTML gerado em `#r-eb` |
| Perfis (Recrutador, Dev, Curioso) | JS, objeto `PF` | `o` = ordem das seções, `h` = texto do destaque, `s` = frase do Sobre mim |
| Mensagens do chat | JS, lista `MS` | `[usuário fictício, mensagem]` |

### Receitas rápidas

**Atualizar o curso da Alura (Python: Crie a sua primeira aplicação):** na lista `CT`, primeira linha, troque o `25` pela nova porcentagem e ajuste o texto (`'Em andamento · 25% · 8h'`).

**Quando concluir o curso:** na `CT`, troque o rótulo para `'Concluído'` e a porcentagem para `100`. Depois adicione o certificado na lista `CQ`.

**Adicionar um projeto novo:** na lista `PR`, copie uma linha, troque o `id` (sem espaços, único) e os textos. O card, a busca e o player passam a funcionar sozinhos.

---

## Como publicar

1. Crie um repositório no GitHub e envie `index.html` e `README.md`.
2. No Netlify, escolha "Add new site" > "Import from Git" (ou arraste a pasta) e publique.
3. Cole os links no topo deste README e na entrega da professora.

---

## Onde parei (atualizado em 03/11/2026)

**Feito**
- [x] Conceito, paleta, tipografia e estrutura definidos
- [x] Site completo com as 6 interações: perfil, player, chat simulado, modo cinema, busca com `/` e "Minha lista", barra de progresso
- [x] Troca da cor de destaque (rosa > cinza > azul gelo)
- [x] QA completo (desktop e celular) e correção do header em 390px
- [x] Curso da Alura em andamento adicionado (25%)
- [x] Código comentado
- [x] Referências (8) e identidade visual (IDV) escritas aqui e no doc

**Pendente**
- [ ] Preencher os `[PREENCHER]`: deploy do CineLog, data e link do certificado da Fundação Bradesco, conteúdo de "Em breve"
- [ ] Abrir cada uma das 8 referências abaixo e anexar um print de cada (o PDF pede referências visuais)
- [ ] Subir no GitHub e publicar no Netlify
- [ ] Reflexão final: o que ficou como imaginei e o que ainda mudaria
- [ ] Slides curtos para a apresentação

**Problemas conhecidos (ainda não corrigidos)**
- Busca sem resultado deixa a tela vazia, sem mensagem
- Clicar fora do painel do player não fecha (só o botão Fechar e a tecla Esc)
- O quadro animado do destaque fica vazio por cerca de 1 segundo ao carregar
- Em telas de 320px o header tem 3 linhas (não cobre o conteúdo)
- Fontes e links externos não foram verificados no ambiente de teste: conferir no navegador

---

## Referências visuais

Nenhum elemento visual foi copiado: aproveitei apenas o comportamento. Prints de cada referência: [PREENCHER]

| # | Referência | O que aproveitei | Onde usei | Link |
|---|---|---|---|---|
| 1 | Netflix: tela "Quem está assistindo?" | Escolher um perfil logo na entrada, com cada perfil mudando a experiência | Seleção de perfil que reordena a página (Recrutador, Dev, Curioso) | https://help.netflix.com/en/node/10421 |
| 2 | Netflix: "Minha lista" e "Continue assistindo" | Salvar itens para ver depois e retomar o que está em andamento | Seção "Minha lista" e fileira "Continue assistindo" | https://www.netflix.com |
| 3 | YouTube: capítulos na barra de progresso | Barra dividida em trechos, com o título do capítulo ao passar o mouse | Barra de progresso do scroll e capítulos do player de projeto | https://mobilesyrup.com/2020/05/28/youtube-video-chapters/ |
| 4 | YouTube e Twitch: modo teatro | Vídeo em destaque, interface em segundo plano e chat ao lado | Modo cinema do player | https://www.youtube.com e https://www.twitch.tv |
| 5 | Twitch: chat lateral ao vivo | Chat ao lado do vídeo, com reações rápidas e emotes | Chat simulado lateral com reações de emoji | https://www.twitch.tv |
| 6 | Meridian (extensão de chat): emotes flutuantes | Emotes que flutuam sobre o player quando o chat acelera | Reações flutuantes ao clicar nos emojis | https://usemeridian.netlify.app/ |
| 7 | Google Fonts: Plus Jakarta Sans | Sans geométrica e moderna, em peso forte nos títulos | Títulos e interface | https://fonts.google.com/specimen/Plus+Jakarta+Sans |
| 8 | JetBrains Mono | Monoespaçada, com cara de dado técnico | Metadados como "T1 · EP1 · 2026" | https://www.jetbrains.com/lp/mono/ |

---

## Identidade visual (IDV)

O conceito é um canal de streaming original, escuro e limpo, que deixa o conteúdo em destaque. O destaque principal começou rosa (`#FF3D71`), passou por cinza (`#8B9099`) e terminou em azul gelo (`#A9C8F5`), como registrado nos ajustes 1 a 4.

### Paleta (variáveis no bloco `Tokens` do CSS)

| Cor | Hex | Variável | Papel | Por que combina |
|---|---|---|---|---|
| Preto profundo | `#0A0A0F` | `--bg` | Fundo | Escuro como as plataformas de vídeo, faz capas e destaques saltarem |
| Grafite | `#16161F` | `--sf` | Cards e superfícies | Separa os blocos do fundo sem bordas fortes |
| Branco gelo | `#F4F4F8` | `--tx` | Texto principal | Leitura confortável no escuro |
| Cinza lilás | `#9A9AB0` | `--mu` | Texto secundário e metadados | Hierarquia entre título e detalhe |
| Azul gelo | `#A9C8F5` | `--co` | Destaque principal | Leve e "clean", com bom contraste |
| Menta elétrica | `#3DF5C8` | `--mn` | Destaque secundário | Toque vivo que equilibra o azul |

Todos os pares de texto e fundo testados ficaram acima de 4,5:1 de contraste.

### Tipografia
- **Plus Jakarta Sans:** títulos e interface, peso forte e espaçamento justo (clima de rede social e streaming).
- **JetBrains Mono:** metadados e rótulos (ar de ficha técnica).

### Tom e personalidade
Moderno, rápido, bem-humorado e direto, em primeira pessoa. Aparece na linguagem de plataforma dos botões ("Assistir agora", "Minha lista"), em "Quem está na sala?" e no chat simulado.

### Estrutura da página
1. Seleção de perfil: a página se adapta a quem visita.
2. Destaque (CineLog): mostra logo o projeto principal.
3. Projetos: o conteúdo central, em formato de séries.
4. Skills por gênero: o que sei, organizado por área.
5. Continue assistindo: o que estou estudando agora e o progresso.
6. Conquistas: certificados com link para a credencial.
7. Em breve: o canal continua crescendo.
8. Sobre mim: apresentação pessoal, como episódio piloto.
9. Contato (Siga o canal): links das redes.

---

## Prompts utilizados

### Fase de planejamento (minhas mensagens, exatamente como escritas)

1. > cloud estou querendo criar um portfolio interativo, tenho uma ideia mas quero caprichar mais.
   > https://manuelcedricgoco.netlify.app/
   > essa é a ideia que pensei por cima, mas quero algo ainda mais interativo, vou te mandar um pdf do que a professora pediu para que tenha nesse portifolio
2. > quero algo moderno com interações criativas, que sejam diferentes das apresentadas com inteligencias artificiais, quero fazer tudo aqui pelo claude
3. Escolha de conceito: **"Mesa de trabalho física"**
4. > Lembrando, preciso apresentar tudo no trabalho depois, podemos colocar um javascript para ter mais interação
5. > quero algo moderno, tipografia de redes sociais e plataformas de stremes. Pensando melhor e se fizessemos um portifolio como uma plaforma de streaming, nada IGUAL a uma especifica quero ainda mais interativo do que uma plataforma comum
6. Dados pessoais enviados: nome (Rhuan Camargo), estudante de engenharia de software, front-end (grid, Tailwind, Bootstrap, vibecode), JavaScript (React, APIs, Git e GitHub), Python, Java básico, SQL e MySQL, C com protoboard, e skills de marketing digital, e-commerce e comunicação assertiva. Depois enviei o link do GitHub e os certificados do LinkedIn. *(resumido aqui por tamanho)*
7. > manda baça

### Prompt inicial (enviado à IA para gerar o site)

> Observação: o prompt foi escrito com ajuda do Claude a partir das minhas respostas acima. A cópia que colei na conversa foi cortada no final (terminava em "separando CSS"). Abaixo está o texto completo.

```
Crie um portfólio pessoal em um único arquivo index.html (HTML, CSS e JavaScript puro, sem frameworks, pronto para deploy no Netlify). O portfólio é um CANAL DE STREAMING fictício, com visual 100% original: não use nome, logo, cor, fonte, ícone ou imagem de nenhuma plataforma real. Idioma: português do Brasil.

QUEM SOU
Rhuan Camargo, estudante de Engenharia de Software. Marca do canal: "Canal RC" (somente texto estilizado, sem logo copiado). Use APENAS as informações abaixo; não invente projetos, métricas, depoimentos ou empresas. Onde faltar dado, deixe o texto [PREENCHER].

CONCEITO E LINGUAGEM
Projetos são séries, skills são gêneros, experiências e cursos são "Continue assistindo", eventos e conquistas são "Ao vivo / Em breve". Botões e rótulos usam linguagem de plataforma ("Assistir agora", "Pular introdução", "Minha lista", "Modo cinema"). Tom: moderno, rápido, bem-humorado e direto, em primeira pessoa.

IDENTIDADE VISUAL
Cores (use como variáveis CSS):
- #0A0A0F fundo; #16161F cards e superfícies; #F4F4F8 texto principal; #9A9AB0 texto secundário;
- #FF3D71 destaque principal (selo AO VIVO, botão principal); #3DF5C8 destaque secundário (progresso, hover, reações).
Tipografia (Google Fonts, com fallback): Plus Jakarta Sans para títulos e interface, em peso forte e espaçamento justo; JetBrains Mono para metadados (ex.: "T1 · EP3 · 2026"); números do ranking em extra-bold bem grandes.
Capas dos projetos: gere com CSS/SVG (gradientes, formas e tipografia), sem imagens externas.

ESTRUTURA (nesta ordem)
1. Tela de seleção de perfil: Recrutador, Dev ou Curioso. Cada perfil reordena as fileiras e muda os destaques e o tom dos textos. Salvar a escolha no localStorage (com try/catch).
2. Hero com a série em destaque: CineLog, com prévia animada em CSS e botões "Assistir" e "+ Minha lista".
3. Fileira "Projetos".
4. Fileira "Skills por gênero".
5. "Continue assistindo" (cursos e estudos, com barra de progresso).
6. "Conquistas" (certificados).
7. "Em breve" (próximos projetos, marcados como em andamento).
8. "Sobre mim" como episódio piloto.
9. Contato como "Siga o canal".

CONTEÚDO REAL
Projetos:
- CineLog (repo: https://github.com/RhuanSantosDev/Projeto-CP3-JS): diário cinematográfico com lista de filmes em que é possível adicionar, retirar e editar os favoritos. Tecnologias: JavaScript, CSS. Link de deploy: [PREENCHER].
- Projeto-curso-ALURA (https://github.com/RhuanSantosDev/Projeto-curso-ALURA): projeto do curso de Git e GitHub, compartilhando e colaborando em projetos. HTML.
- Aprenda-Pull-Request (https://github.com/RhuanSantosDev/Aprenda-Pull-Request): fork para praticar pull requests.
- Estudos de base: repositórios webdev, aula-3 e aula-de-html-e-css (primeiros passos em HTML e CSS).
Skills (gêneros):
- Front-end: HTML, CSS, grid, Tailwind, Bootstrap, vibecoding.
- JavaScript: React, consumo de APIs (adicionar e remover informações em sites), Git e GitHub.
- Back e dados: Python (listas e fundamentos), SQL e MySQL (criar e alterar tabelas, inserir e remover dados), Java (básico: classes e orientação a objetos), C (projetos de sala com protoboard, nível básico).
- Negócios e pessoas: marketing digital, e-commerce, comunicação assertiva.
Conquistas (cada card com botão "Ver credencial"):
- Git e GitHub, Alura, set. 2026: https://cursos.alura.com.br/certificate/bc76981c-15e7-4db8-a5de-6a32edbbb5a3?lang
- Algoritmos: Aprenda a programar, FIAP, mar. 2026: https://on.fiap.com.br/local/nanocourses/gerar_certificado.php?chave=485efcbeaba48a7f64515b9be8859047&action=view
- Design Thinking, FIAP, mar. 2026: https://on.fiap.com.br/local/nanocourses/gerar_certificado.php?chave=ce97e9809bba2c45970b67031f19facf&action=view
- Agentes Autônomos (Agentic AI), FIAP, mar. 2026: https://on.fiap.com.br/local/nanocourses/gerar_certificado.php?chave=0226d2bf01e73b60debc274170ec1ee0&action=view
- Formação Social e Sustentabilidade, FIAP, mar. 2026: https://on.fiap.com.br/local/nanocourses/gerar_certificado.php?chave=19a56f753ad7d26dbbdcf07f06b29e92&action=view
- Modelagem de Dados, Fundação Bradesco, [MÊS/ANO], link [PREENCHER].
Contato: GitHub https://github.com/RhuanSantosDev, LinkedIn https://www.linkedin.com/in/rhuan-santos-, Instagram https://www.instagram.com/_rhuancamargo/.

INTERAÇÕES (implemente exatamente estas 6, bem feitas)
1. Seleção de perfil que reordena a página, como descrito.
2. Player de projeto: ao clicar em "Assistir", o projeto abre como episódio em modal, com capítulos clicáveis, botão "Pular introdução" e botão de fechar (Esc também fecha).
3. Chat ao vivo lateral: mensagens curtas e bem-humoradas de espectadores fictícios comentando a página, com reações flutuantes (emoji) ao clicar. Deixe claro que é uma simulação (selo "chat simulado") e não atribua elogios a pessoas ou empresas reais.
4. Modo cinema: apaga a luz da página e destaca só o projeto aberto.
5. Busca com atalho "/" e "Minha lista": adicionar e remover itens favoritos, salvos no localStorage (com try/catch).
6. Barra de progresso do scroll no topo, como linha do tempo de vídeo, com capítulos clicáveis que levam às seções.

REQUISITOS TÉCNICOS
- Responsivo (celular, tablet, desktop). Fileiras com scroll horizontal por toque e por botões de seta.
- Acessível: navegação completa por teclado, foco visível, aria-labels, contraste adequado e respeito a prefers-reduced-motion.
- Sem erros no console. Todos os botões e links precisam funcionar.
- Código organizado, com comentários curtos separando CSS e JS por seção.
```

### Prompts de ajuste, em ordem, com registro de correção

**Ajuste 1: cor de destaque**
- **Prompt:** `ta ficando legal, quero que mude essa cor "rosa" para um cinza espacial como o cinza dos carros atuais, é um cinza igual aos carros novos da Volkswagen`
- **Problema:** o rosa (`#FF3D71`) não era a cor que eu queria.
- **Resultado:** resolveu em parte. Troquei para cinza `#8B9099`, mas não gostei.
- **Aprendizado:** definir a cor de destaque com referência visual (foto, nome da cor) já no prompt inicial.

**Ajuste 2: o cinza ficou "inacabado"**
- **Prompt:** `nao sei se gostei, ficou como algo que ainda nao esta pronto, sabe?`
- **Problema:** o cinza chapado se misturou com textos e bordas, e a página perdeu o ponto de foco.
- **Resultado:** a IA explicou a causa e sugeriu alternativas (prata metálica, azul gelo).
- **Aprendizado:** o destaque precisa contrastar com o texto secundário. Descrever a sensação ("clean", "leve") ajuda mais que o nome de uma cor.

**Ajuste 3 e 4: cor "clean"**
- **Prompts:** `me da uma cor moderna de sugestao mas nada muito forte, quero uma cor "clean" leve` e depois `manda`
- **Resultado:** resolveu totalmente. Destaque virou azul gelo `#A9C8F5`.
- **Aprendizado:** pedir sugestões antes de aplicar evita retrabalho.

**Ajuste 5: QA completo**
- **Prompt:** `valida todos esses testes pra mim, um por um detalhadamente`
- **Resultado:** 96 verificações automatizadas (desktop e celular). Encontrou o problema do header no celular e três pendências menores (ver "Problemas conhecidos").
- **Aprendizado:** conferir também os prints, não só os números: um dos testes passou por engano e outro falhou por erro do próprio teste.

**Ajuste 6: header no celular**
- **Prompt:** `exato, uma correção por vez, e preciso que o header seja testado em 390px e fique em uma ou duas linhas no máximo.`
- **Problema:** o header quebrava em 3 linhas (151px contra 104px reservados) e cobria o conteúdo.
- **Resultado:** resolveu totalmente em 390px e em 360 a 412px. Em 320px ainda tem 3 linhas, sem cobrir conteúdo.
- **Aprendizado:** no prompt inicial, definir o máximo de linhas do header em 390px e usar ícones nos botões de navegação do celular.

**Atualização de conteúdo e documentação**
- **Prompt:** `estou fazendo esse curso da alura, coloca como em andamento, preciso do site completo todo para eu posta-lo no git hub, quero os prompts que fizeram sentido em um docs a parte para eu mandar para a professora mas coloca eles tambem no redme para eu saber onde parei depois no projeto e onde modificar cada coisa conforme eu for estudando, comenta o que puder para deixar detalhado o projeto e facil de entender`
- **Resultado:** curso "Python: Crie a sua primeira aplicação" (Alura, 25%) adicionado, código comentado e este README criado.

> Mensagens só de navegação (por exemplo, "legal, ta ficando bom, qual proximo passo?") ficaram de fora desta lista.

---

## Reflexão final

[PREENCHER: o que ficou como imaginei e o que ainda mudaria]

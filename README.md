# Corsini Móveis Planejados

Site de apresentação da Corsini Móveis Planejados, em Três Lagoas – MS.
Desenvolvido com HTML, CSS e JavaScript, sem framework e sem etapa de build.

## Estrutura

- `index.html`: conteúdo da página, navegação, formulário e janelas de ampliação.
- `style.css`: layout, cores, componentes, animações e adaptações para celular.
- `fonts.css`: carregamento das fontes utilizadas no projeto.
- `config.js`: contatos e dados do portfólio, organizados por ambiente.
- `app.js`: filtros, galerias, vídeos, ampliação, menu e mensagem de orçamento.
- `assets/images/`: logo, fotos e detalhes extraídos dos vídeos da Corsini.
- `assets/videos/`: quatro vídeos reais do portfólio.
- `.prettierrc.json`: configuração para manter a formatação consistente.

## Como executar

Abra `index.html` no navegador ou use a extensão Live Server no VS Code.

Para servir a pasta usando Python:

```bash
python -m http.server 8000
```

Depois, abra `http://localhost:8000`.

## Como editar

### Portfólio

Edite `window.CORSINI.projects` em `config.js`. Cada categoria contém título,
descrição, link da publicação original e uma lista de mídias.

- `image`: caminho da foto ou da capa, relativo à pasta `assets/`.
- `video`: caminho opcional do vídeo, relativo à pasta `assets/`.
- `title`: legenda do visual.
- `still`: indica uma imagem extraída de um vídeo.
- `url`: publicação original específica, quando diferente do link da categoria.

Mantenha os filtros de `index.html` alinhados aos nomes das categorias.

### Contatos

O WhatsApp usado na mensagem de orçamento vem de `config.js`.
Ao alterar o telefone, endereço ou redes sociais, atualize também os links e
textos correspondentes em `index.html`, incluindo o botão flutuante.

### Aparência

As variáveis de cores e tipografia ficam no início de `style.css`.
As adaptações por largura de tela e o tratamento de movimento reduzido estão
identificados no arquivo. `fonts.css` reúne o carregamento das fontes.

## Funcionalidades

- Galerias filtráveis por ambiente, com 18 fotos e vídeos.
- Quatro vídeos em loop, com reprodução automática sem som quando visíveis.
- Controles para áudio e reprodução; respeito à preferência por movimento reduzido.
- Janela de ampliação com navegação pelos exemplos do mesmo ambiente.
- Galerias com deslize lateral no celular.
- Menu responsivo, perguntas frequentes e links para contato e localização.
- Formulário que prepara uma mensagem no WhatsApp para o visitante revisar e enviar.

## Dados e imagens

O formulário não possui backend nem banco de dados. O site não confirma o envio
pelo WhatsApp; o visitante conclui essa ação no aplicativo.

As imagens e vídeos foram obtidos de publicações públicas da Corsini.
As legendas identificam os detalhes extraídos de vídeos. Esses visuais mostram
ângulos dos projetos e não representam 18 projetos diferentes.

Antes do lançamento comercial, confirme os contatos, a disponibilidade do
WhatsApp e a autorização da empresa para uso dos materiais. Prefira fotos
originais em alta resolução quando fornecidas pelo cliente.

As fontes são carregadas pelo Google Fonts. WhatsApp, Instagram e Google Maps
são serviços externos.

## Publicação

O conteúdo da raiz pode ser usado em qualquer hospedagem de arquivos estáticos.
Não é necessário instalar dependências para executar o site.

## Formatação

Os arquivos estão formatados com indentação de dois espaços, propriedades CSS
em linhas separadas e HTML organizado, inclusive nos templates JavaScript.

Para repetir a formatação, opcionalmente execute:

```bash
npx prettier --write index.html style.css fonts.css config.js app.js
```

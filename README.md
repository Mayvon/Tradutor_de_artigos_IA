# Descrição do Projeto: Tradutor de Artigos da Web com Azure OpenAI

Este projeto foi criado durante o DIO Bootcamp Microsoft #102 combinando a extração de textos de páginas da web em inglês com a tradução automática para o português através da implementação da Azure OpenAI

## O que este projeto faz?

1. **Extrai texto de uma página da web:**
   - Dado um link (URL), o código acessa a página e utiliza a biblioteca `BeautifulSoup` para pegar o conteúdo de texto principal, removendo scripts, estilos e outros elementos desnecessários.
   - O texto extraído é "limpo", organizado em linhas e fica pronto para ser usado.

2. **Traduz o conteúdo:**
   - O texto extraído é enviado para a API do Azure OpenAI, que realiza a tradução para o idioma especificado (neste caso, o português).

3. **Exporta o texto traduzido:**
   - O texto traduzido é formatado em Markdown, útil para publicação em blogs ou uso em documentação.

## Principais Bibliotecas Utilizadas

- **`requests`:** Para acessar o conteúdo da página web.
- **`beautifulsoup4`:** Para processar o HTML e extrair o texto.
- **`langchain-openai`:** Para integração com a API de tradução do Azure OpenAI.

## Como usar este script?

1. **Instale as dependências:**
   - Execute este comando para instalar as bibliotecas necessárias:
     ```bash
     pip install requests beautifulsoup4 openai langchain-openai
     ```

2. **Configure as credenciais da API do Azure OpenAI:**
   - Substitua as seguintes variáveis com suas informações do Azure:
     ```python
     azure_endpoint = "SEU_ENDPOINT_AQUI"
     api_key = "SUA_CHAVE_AQUI"
     api_version = "SUA_VERSAO_AQUI"
     deployment_name = "NOME_DA_VERSAO_AQUI"
     ```

3. **Defina a URL do artigo:**
   - Substitua `"URL_AQUI"` pelo link da página que deseja traduzir.

4. **Execute o script:**
   - O código extrairá o texto da página, traduzirá para o português e exibirá o resultado no formato Markdown.

## Exemplo de Entrada e Saída

- **Entrada:**
  URL de uma página web contendo um artigo em inglês.

- **Saída:**
  Texto traduzido para português, formatado em Markdown.

## Aprendizados 

- **Manipulação de HTML:** Como usar o `BeautifulSoup` para extrair textos úteis de páginas web.
- **Integração com APIs:** Como configurar e usar o Azure OpenAI para tarefas de tradução.
- **Automatização de Tarefas:** Criar um fluxo simples de extração e tradução de textos da web.

## Possíveis Melhorias 

- Adicionar suporte para mais idiomas.
- Salvar o texto traduzido em um arquivo `.md` ou `.txt`.
- Melhorar o tratamento de erros, como links inválidos ou limitações de API.


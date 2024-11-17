# genai-maintenance-study

## Descrição

Este projeto tem como objetivo a implementação de um estudo sobre IA generativa para a avaliação de aderência em planos de manutenção. Para o desenvolvimento, o projeto utilizou o GPT-4o Mini por meio da Azure OpenAI e o framework [Langchain](https://www.langchain.com/) para o desenvolvimento de código, automatizando verificações, reduzindo a subjetividade e aumentando a precisão. A solução proposta consiste em uma ferramenta para automatizar verificações e análises em planos de manutenção.

---

## Índice

- [Pré-requisitos](#pré-requisitos)
- [Configuração do Azure OpenAI](#configuração-do-azure-openai)
- [Configuração do Arquivo .env](#configuração-do-arquivo-env)
- [Como Executar o Projeto](#como-executar-o-projeto)

---

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte:

1. Conta no [Portal do Azure](https://portal.azure.com/).
2. Chave de API do Azure OpenAI.
3. Configuração do Ambiente
    - Este projeto disponibiliza arquivo .yml para configuração de ambiente, portanto recomenda-se utilizar ferramenta anaconda/miniconda para configuração do ambiente.
      1. Ter [Miniconda](https://docs.anaconda.com/miniconda/) instalado no sistema operacional.
      2. Utilizar o arquivo `environment.yml`, disponível neste repositório, para configurar automaticamente o ambiente do projeto.
      3. Para configurar o ambiente, execute
         ```plaintext
         conda env create -f environment.yml

---

## Configuração do Azure OpenAI

### Como criar e implantar um recurso do Serviço OpenAI do Azure

Para utilizar o Azure OpenAI, é necessário obter uma chave de API que permitirá a autenticação e o acesso aos serviços. Siga os passos abaixo:

1. **Crie uma conta no Azure:**
   - Se ainda não possui, registre-se no [Portal do Azure](https://portal.azure.com/).

2. **Crie um recurso do Azure OpenAI:**
   - No portal do Azure, clique em **"Criar um recurso"** e procure por **"Azure OpenAI"**.
   - Selecione **"Azure OpenAI"** e clique em **"Criar"**.
   - Preencha os campos necessários, como assinatura, grupo de recursos, região e nome do recurso.
   - Após preencher todas as informações, clique em **"Revisar + criar"** e, em seguida, em **"Criar"**.

3. **Recupere a chave de API:**
   - Após a implantação do recurso, navegue até ele no portal do Azure.
   - No menu lateral, selecione **"Chaves e Ponto de Extremidade"**.
   - Você verá duas chaves primárias (**KEY1** e **KEY2**).
   - Copie uma dessas chaves; ela será sua chave de API para autenticação nas chamadas à API do Azure OpenAI.

Para mais detalhes, consulte a [documentação oficial](https://learn.microsoft.com/pt-br/azure/).

---

## Configuração do Arquivo .env

O código utiliza um arquivo `.env` para configurar as variáveis de ambiente necessárias para a execução dos notebooks. Criar arquivo `.env` seguindo o formato descrito abaixo.

### Como configurar o arquivo `.env`

1. No diretório raiz do projeto, crie um arquivo chamado `.env`.
2. Adicione as variáveis necessárias conforme padrão de CHAVE=VALOR abaixo:

   ```plaintext
   AZURE_OPENAI_API_KEY=your-api-key-here
   AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com
   AZURE_OPENAI_API_VERSION=your-api-version
   AZURE_OPENAI_DEPLOYMENT_NAME=your-deployment-model-name
---

## Como Executar o Projeto

Os códigos deste projeto foram desenvolvidos em **notebooks Python** (`.ipynb`).

### Como Executar os Notebooks

Os notebooks podem ser executados utilizando ferramentas como:

1. **Jupyter Notebook ou JupyterLab**.
2. **VS Code** (ou outras IDEs compatíveis com notebooks Python).


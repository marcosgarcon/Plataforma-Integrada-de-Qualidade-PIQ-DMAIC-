# Plataforma Integrada de Qualidade (PIQ-DMAIC)

Este repositório é o centro de um projeto para construir uma plataforma de gestão da qualidade baseada na metodologia DMAIC, utilizando a integração de ferramentas open source.

## Objetivo

O objetivo deste projeto é criar um fluxo de trabalho coeso para projetos de melhoria contínua, onde cada fase do DMAIC é suportada pela melhor ferramenta open source para a tarefa, com os sistemas se comunicando via API e eventos.

## Arquitetura da Solução

A plataforma não busca unificar o código-fonte das ferramentas, mas sim integrá-las através de suas APIs e um ambiente de execução unificado via Docker.

**Fluxo Conceitual:**
`[Gestão de Projetos] <--> [API] <--> [ERP/QMS] <--> [API] <--> [BI/Dashboards]`

### Ferramentas Principais
* **Gestão de Projetos (Definir):** OpenProject
* **ERP & QMS (Melhorar, Controlar):** Odoo
* **Análise Estatística (Medir, Analisar):** Jamovi (Desktop) ou scripts Python/R.
* **Business Intelligence (Controlar):** Metabase
* **Orquestração da Integração:** Scripts Python / Node-RED / n8n

## Como Começar (Ambiente de Desenvolvimento)

Este projeto utiliza Docker e Docker Compose para orquestrar os serviços.

1.  **Pré-requisitos:**
    * [Git](https://git-scm.com/)
    * [Docker](https://www.docker.com/products/docker-desktop/)
    * [Docker Compose](https://docs.docker.com/compose/install/)

2.  **Clone o repositório:**
    ```bash
    git clone [URL_DO_SEU_REPOSITORIO_AQUI]
    cd PIQ-DMAIC
    ```

3.  **Configuração:**
    * Copie os arquivos de exemplo no diretório `config_examples` para seus respectivos locais e ajuste as variáveis (senhas, portas, etc.).
    * Configure as variáveis de ambiente necessárias para os scripts de integração (chaves de API, URLs).

4.  **Inicie os serviços:**
    ```bash
    docker-compose up -d
    ```

    Após a execução, os serviços estarão disponíveis nos seguintes endereços (padrão):
    * **Odoo:** `http://localhost:8069`
    * **Metabase:** `http://localhost:3000`

## Estrutura do Repositório

* **/docker:** Contém os arquivos `docker-compose.yml` para subir o ambiente.
* **/docs:** Documentação detalhada sobre a arquitetura, configuração das APIs e manuais de processo.
* **/integration_scripts:** Contém os scripts (Python, etc.) que fazem a "cola" entre os sistemas.
* **/config_examples:** Exemplos de arquivos de configuração para cada serviço.

# Plataforma-Integrada-de-Qualidade-PIQ-DMAIC-
Ferramenta de gestão de qualidade 

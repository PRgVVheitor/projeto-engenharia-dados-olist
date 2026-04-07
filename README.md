🏗️ Engenharia de Dados com Arquitetura Medalhão — Olist
🧭 Por que esse projeto existe?

A maioria dos dados não falha por falta de volume.
Falha por falta de estrutura.

Empresas acumulam dados todos os dias — mas sem organização, eles não geram decisão, não geram insight e, principalmente, não geram valor.

Este projeto nasce exatamente nesse ponto:

transformar dados brutos em informação confiável, estruturada e pronta para decisão.

🎯 O que foi feito

Foi construído um pipeline de dados ponta a ponta, utilizando o dataset público da Olist, com um objetivo claro:

Organizar dados desde a origem até o consumo
Garantir qualidade e consistência ao longo do processo
Entregar uma base analítica pronta para uso

Mas mais importante do que o que foi feito é como isso foi pensado.

⚙️ Como isso foi construído

A base do projeto é a arquitetura medalhão.

Mas não como um conceito teórico — e sim como uma estratégia de controle de qualidade do dado.

Cada camada tem um papel claro no fluxo:

🥉 Bronze — Capturar a realidade

Aqui, o foco não é tratar. É preservar.

Ingestão dos dados brutos
Padronização mínima
Armazenamento fiel à origem

📄 Atividade_land_to_bronze.ipynb

👉 Se o dado chegar errado aqui, tudo depois nasce comprometido.

🥈 Silver — Construir confiança

Aqui, o dado começa a fazer sentido.

Limpeza e tratamento
Remoção de duplicidades
Padronização de colunas
Estruturação em dimensões e fatos

📄 Atividade_bronze_to_silver.ipynb

👉 Essa é a camada onde o dado deixa de ser risco e passa a ser confiável.

🥇 Gold — Gerar decisão

Agora o foco muda: não é mais engenharia, é negócio.

Tabelas agregadas
Modelagem analítica
Otimização para consultas

📄 Atividade_silver_to_gold.ipynb

👉 Aqui, o dado responde perguntas reais.

🔄 O pipeline como sistema confiável

Pipeline que roda uma vez não vale nada.

O valor está em rodar sempre, do jeito certo.

Por isso, a execução foi orquestrada via Databricks Jobs, respeitando dependências:

Bronze → Silver → Gold

📄 job.yaml

👉 Isso garante consistência, reprocessamento e escalabilidade.

⚙️ Tecnologias utilizadas
Databricks → ambiente de execução e orquestração
PySpark → processamento distribuído
Delta Lake → armazenamento confiável e versionado
GitHub → versionamento e organização do projeto

📸 Execução do pipeline

📂 Estrutura do repositório
📁 projeto
 ├── Atividade_land_to_bronze.ipynb
 ├── Atividade_bronze_to_silver.ipynb
 ├── Atividade_silver_to_gold.ipynb
 ├── job.yaml
 └── pipeline_execucao.png
✅ O que esse projeto demonstra

Esse projeto não é só sobre tecnologia.

Ele demonstra:

Capacidade de estruturar dados de ponta a ponta
Entendimento prático de arquitetura medalhão
Organização orientada a consumo analítico
Pensamento de engenharia aplicado ao negócio
📌 No fim, tudo se resume a isso

Dados brutos são apenas registros.

Dados organizados são ativos.

E ativos bem estruturados se transformam em decisão.

Esse projeto é a transição entre esses três estágios.

👨‍💻 Autor

Heitor Araujo

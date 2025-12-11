🎯 MVP: Previsão de Churn de Clientes
Este projeto consiste na construção de um Mínimo Produto Viável (MVP) para prever se um cliente irá cancelar os serviços (Churn) ou continuar, utilizando um modelo de Machine Learning (Random Forest) e disponibilizando o resultado via um modelo serializado, pronto para ser integrado em uma API.



Público: alunos iniciantes em tecnologia, sem experiência profissional na área, mas que já estudaram Back-end com Java (APIs REST, persistência, testes) e Data Science (Python, Pandas, scikit-learn, ML supervisionado).

Objetivo: construir, em grupo, um MVP (mínimo produto viável) capaz de prever se um cliente vai cancelar e disponibilizar essa previsão via uma API funcional.

Escopo ideal: classificação binária (“vai cancelar” / “vai continuar”) com base em um dataset pequeno e limpo.

Entregáveis desejados

Notebook (Jupyter/Colab) do time de Data Science, contendo:

Exploração e limpeza dos dados (EDA);

Engenharia de features (ex.: tempo de uso, frequência de login, histórico de pagamento);

Treinamento de modelo supervisionado (ex.: Logistic Regression, Random Forest);

Métricas de desempenho (Acurácia, Precisão, Recall, F1-score);

Serialização do modelo (joblib/pickle).

Aplicação Back-End (API REST) do time de Java:

Endpoint que recebe informações de um cliente e retorna a previsão do modelo (Ex.: “Vai cancelar” / “Vai continuar”);

Integração com o modelo de DS (direta ou via microserviço Python);

Logs e tratamento de erros.

Documentação mínima (README):

Como executar o modelo e a API;

Exemplos de requisição e resposta (JSON);

Dependências e versões das ferramentas.

Demonstração funcional (Apresentação curta):

Mostrar a API em ação (via Postman, cURL ou interface simples);

Explicar como o modelo chega à previsão.

Funcionalidades exigidas (MVP)

O serviço deve expor um endpoint que retorna uma previsão sobre o cliente e a probabilidade associada a essa previsão. Exemplo: POST /predict: recebe JSON com dados do cliente e retorna: { "previsao": "Vai cancelar", "probabilidade": 0.76 }

Carregamento de modelo preditivo: o back-end deve ser capaz de acessar o modelo de churn (localmente ou via serviço DS).

Validação de entrada: verificar se todos os campos obrigatórios estão preenchidos.

Resposta estruturada: incluir previsão e probabilidade numérica.

Exemplos de uso: 3 requisições de teste (clientes com e sem cancelamento).

Documentação simples: um README explicando como rodar o projeto e reproduzir os testes.

Funcionalidades opcionais

Endpoint GET /stats: retorna estatísticas básicas, como: { "total_avaliados": 500, "taxa_churn": 0.23 }

Persistência de previsões: armazenar clientes e resultados em banco (H2 ou PostgreSQL).

Dashboard simples (Streamlit ou HTML): visualiza clientes com maior risco.

Explicabilidade básica: incluir no retorno as 3 variáveis mais relevantes para o resultado (ex.: “tempo de contrato”, “atrasos em pagamentos”, “uso do app”).

Batch Prediction: endpoint que aceita lista de clientes (arquivo CSV).

Containerização: rodar o sistema completo com Docker/Docker Compose.

Testes automatizados: unitários e de integração simples (JUnit, pytest).


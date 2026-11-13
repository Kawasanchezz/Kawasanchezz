<div align="center">

# &lt;/&gt; Kawã Sanchez

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=21C063&center=true&vCenter=true&width=760&lines=Desenvolvedor+Backend+J%C3%BAnior;Java+%E2%80%A2+Spring+Boot+%E2%80%A2+APIs+REST;PostgreSQL+%E2%80%A2+Redis+%E2%80%A2+Docker+%E2%80%A2+AWS;Aberto+a+vagas+j%C3%BAnior+ou+est%C3%A1gio+em+Back-end)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kawasanchez)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:kawagarcia71@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000?style=flat-square&logo=vercel&logoColor=white)](https://kawasanchez.vercel.app)

</div>

---

## `> about_me`

```json
{
  "name": "Kawã Sanchez",
  "position": "Desenvolvedor Backend Júnior",
  "location": "São Paulo, SP, BR",
  "education": "Tecnólogo em ADS (concluído) | Ciência da Computação (cursando)",
  "university": "Universidade Cruzeiro do Sul",
  "languages": "Inglês intermediário | Espanhol intermediário",
  "focus": "Back-end com Java, Spring Boot, APIs REST e PostgreSQL",
  "looking_for": "Desenvolvedor Backend Júnior, Engenheiro de Software Júnior ou estágio em Back-end"
}
```

Desenvolvedor Backend Júnior (Java), com foco em Spring Boot, APIs REST e PostgreSQL. Formado em Análise e Desenvolvimento de Sistemas e cursando Ciência da Computação na Universidade Cruzeiro do Sul.

Construo APIs REST com Spring Boot, PostgreSQL e Redis, com testes de integração (Testcontainers), CI no GitHub Actions e análise de segurança (CodeQL), usando Git e GitHub no dia a dia. Cada projeto traz no README as decisões de projeto e as limitações conhecidas.

Antes de programar, atuei 2 anos como designer gráfico e suporte de TI, o que me deu comunicação com o cliente e atenção ao que o negócio realmente precisa.

## `> featured_projects`

### [FraudGuard: antifraude em tempo real](https://github.com/Kawasanchezz/fraudguard)

Avalia cada transação (Pix, cartão, transferência) e responde APROVAR, REVISAR ou BLOQUEAR com score e motivos. Regras independentes (padrão Strategy), versionadas e alteráveis sem deploy; janela deslizante no Redis; fail-safe com timeout e circuit breaker (Resilience4j) quando o Redis cai; decisão idempotente, também via fila (SNS + SQS no LocalStack, com DLQ); fila de revisão manual e relatório de falsos positivos e negativos por versão de regras. Métricas com Prometheus e Grafana. Testes com Testcontainers e cobertura mínima de 85% (JaCoCo). Projeto acadêmico: a meta de p95 abaixo de 100 ms não foi atingida no meu ambiente, e o resultado está documentado no README.

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### [Core Banking: contas e transações](https://github.com/Kawasanchezz/core-banking-ledger)

API REST de core banking com ledger de dupla entrada: depósito, saque, transferência, saldo e extrato. Transações ACID, concorrência com lock pessimista em ordem de id (sem deadlock) e `@Version` como segunda barreira, idempotência por `Idempotency-Key` e conferência de reconciliação do saldo. Segurança com JWT, BCrypt, limite de tentativas de login e CPF mascarado em logs. Testado com 300 transferências cruzadas em 8 threads, sem deadlock nem saldo negativo, e Testcontainers com PostgreSQL real. Projeto acadêmico; limitações documentadas no SECURITY.md.

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### [CreditFlow: simulador e esteira de crédito](https://github.com/Kawasanchezz/creditflow)

Simula empréstimos (tabelas Price e SAC), analisa o risco por uma cadeia de regras (Chain of Responsibility), aprova ou recusa e contrata de forma idempotente, gerando o cronograma de parcelas. Cálculo com BigDecimal e arredondamento bancário, CET aproximado por TIR e integração resiliente com serviço de score (retry e fallback para análise manual), testada com WireMock. Testes parametrizados, de propriedade e de integração, com cobertura mínima de 90% nas regras de negócio, e CI com GitHub Actions. Projeto acadêmico.

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### [Motor de Regras para Notificações](https://github.com/Kawasanchezz/Motor-de-Regras-para-Notificacoes)

Serviço backend que decide se, quando e por qual canal enviar uma notificação, com regras configuráveis em tempo de execução, sem deploy. Condições em árvore AND/OR (JSONB) e restrições de cooldown, rate limit, janela de horário, deduplicação e opt-out. Idempotência por evento, auditoria de cada decisão e fila de agendamento no Redis, segura para várias instâncias. Extensível: novo operador, restrição ou canal é uma nova classe. API documentada com Swagger e métricas com Actuator e Prometheus.

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

### [TreeBOM: lista de materiais](https://github.com/Kawasanchezz/ProjetosEstruturadeDados-V2)

Sistema de Lista de Materiais (BOM) com árvore genérica implementada à mão: explosão da estrutura, simulação de produção para N unidades e implosão de custos. Quando o preço de um componente muda, o custo sobe até a raiz com algoritmos iterativos (sem recursão), testado com uma árvore de 5.000 níveis. BigDecimal para valores monetários, validação de ciclo, pai inexistente e raiz duplicada, e login com JWT e perfis de admin e leitura. Backend migrado de Python (FastAPI) para Java, mantendo o mesmo contrato de API. Projeto acadêmico.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

### [Astra: assistente de IA](https://github.com/Kawasanchezz/Astra) · [demo](https://astra-nine-omega.vercel.app)

Assistente de IA em português para dúvidas de estudo e programação, por texto ou voz. API em Flask integrada a um LLM (Groq), com prompt de sistema para responder no idioma do usuário, rate limiting por minuto e por dia, validação do tamanho da entrada, CORS restrito, checagem de origem e mascaramento de segredos. A chave de API fica em variáveis de ambiente e há modo de demonstração sem chave. CI com GitHub Actions, CodeQL e Dependabot. Publicado na Vercel. Projeto pessoal.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)

## `> experience`

**Designer gráfico assistente · Polyscreen Signs** (set/2023 – set/2025)

- Criação de banners, logotipos e artes para clientes, traduzindo cada pedido em peças prontas para produção.
- Levantamento de requisitos com mais de 20 clientes e stakeholders, transformando necessidades de negócio em especificações e prazos de entrega.
- Padronização de arquivos e bases, com controle de versão e de acesso: busca de arquivos reduzida de cerca de 10 para 3 minutos (-70%).
- Consultas em SQL e planilhas de pedidos e de controle de estoque, reduzindo o retrabalho da equipe.
- Suporte de TI à equipe, garantindo a continuidade da operação no dia a dia.

## `> tech_stack`

#### Languages
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)

#### Backend & APIs
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![REST](https://img.shields.io/badge/API_REST-02569B?style=flat&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Resilience4j](https://img.shields.io/badge/Resilience4j-4B8BBE?style=flat&logoColor=white)

#### Databases
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat&logo=flyway&logoColor=white)

#### Testing, CI & Cloud
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=flat&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-9B2C8E?style=flat&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![CodeQL](https://img.shields.io/badge/CodeQL-181717?style=flat&logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)

#### Front-end (complementar)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css&logoColor=white)

#### IA (complementar)
![LLM](https://img.shields.io/badge/LLM-412991?style=flat&logoColor=white)
![Amazon Bedrock](https://img.shields.io/badge/Amazon_Bedrock-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-F7931E?style=flat&logoColor=white)

## `> certifications`

| Emissor | Certificações |
| :--- | :--- |
| ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white) | Cloud Solutions Architect · Generative AI and AI Agents with Amazon Bedrock · Cloud Support Associate · Cloud Technology Consultant |
| ![Meta](https://img.shields.io/badge/Meta-0467DF?style=flat&logo=meta&logoColor=white) | Back-End Developer · Full Stack Developer · Front-End Developer |
| ![Microsoft](https://img.shields.io/badge/Microsoft-5E5E5E?style=flat&logo=microsoft&logoColor=white) | Back-End Developer · Full-Stack Developer · Front-End Developer · Data Analysis with SQL, Excel & Power BI |
| ![IBM](https://img.shields.io/badge/IBM-052FAD?style=flat&logo=ibm&logoColor=white) | Full-Stack JavaScript Developer · Machine Learning |
| ![Vanderbilt University](https://img.shields.io/badge/Vanderbilt_University-866D4B?style=flat&logoColor=white) | AI Agent Developer |
| ![Google](https://img.shields.io/badge/Google-4285F4?style=flat&logo=google&logoColor=white) | IT Support Professional |
| ![DIO](https://img.shields.io/badge/DIO-FF2D6F?style=flat&logoColor=white) | Bootcamp Itaú: Java com Inteligência Artificial · Introdução à Plataforma Java |
| ![Fundação Bradesco](https://img.shields.io/badge/Funda%C3%A7%C3%A3o_Bradesco-CC092F?style=flat&logoColor=white) | Segurança em Tecnologia da Informação · Lei Geral de Proteção de Dados (LGPD) · Implementando Banco de Dados · Administrando Banco de Dados · Modelagem de Dados · Introdução à Programação Orientada a Objetos (POO) |

## `> git_stats`

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Kawasanchezz&theme=dark&hide_border=true&locale=pt_BR)](https://git.io/streak-stats)

</div>

---

<div align="center">

![Visitors](https://komarev.com/ghpvc/?username=Kawasanchezz&color=21C063&style=flat-square&label=Visitors)

</div>

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Kawasanchezz/Kawasanchezz/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Kawasanchezz/Kawasanchezz/output/github-contribution-grid-snake.svg" />
  <img alt="Animação da cobra percorrendo o gráfico de contribuições" src="https://raw.githubusercontent.com/Kawasanchezz/Kawasanchezz/output/github-contribution-grid-snake.svg" />
</picture>

</div>

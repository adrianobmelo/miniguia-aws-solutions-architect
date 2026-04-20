# ☁️ Miniguia de Estudos — AWS Certified Solutions Architect Associate (SAA-C03)

> Projeto desenvolvido como entrega do Desafio de Projeto da DIO, utilizando o NotebookLM como ferramenta de aprendizagem ativa com curadoria de fontes, engenharia de prompts e produção de um miniguia temático.

---

## 📌 Contexto e Objetivos

### Assunto Escolhido
**Certificação AWS Certified Solutions Architect – Associate (SAA-C03)**

A certificação AWS Solutions Architect Associate é uma das mais reconhecidas e valorizadas no mercado de cloud computing. Ela valida a capacidade de projetar sistemas distribuídos resilientes, de alta performance, seguros e com custo otimizado na plataforma da Amazon Web Services.

### Objetivos de Estudo

- Compreender os **domínios da prova SAA-C03** e o peso de cada um na avaliação.
- Identificar os **serviços AWS mais cobrados** e entender seus casos de uso.
- Desenvolver raciocínio arquitetural para cenários de **alta disponibilidade, escalabilidade e segurança**.
- Criar material de revisão rápida com **glossário e resumos** para consulta antes da prova.
- Utilizar o NotebookLM para transformar fontes técnicas em um caderno de estudos interativo.

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas por sua relevância técnica, atualidade e alinhamento com o exame SAA-C03. Todas foram inseridas no NotebookLM para análise e geração de insights.

| # | Fonte | Descrição | Link |
|---|-------|-----------|------|
| 1 | **AWS Exam Guide SAA-C03** | Guia oficial da Amazon com os domínios, pesos e tipos de questões da prova | [🔗 Acessar](https://d1.awsstatic.com/pt_BR/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf) |
| 2 | **AWS Well-Architected Framework Whitepaper** | Whitepaper oficial com os 6 pilares de arquitetura AWS | [🔗 Acessar](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) |
| 3 | **AWS Architecture Center** | Diagramas de referência e boas práticas de arquitetura por setor | [🔗 Acessar](https://aws.amazon.com/architecture/) |
| 4 | **Tutorialsdojo SAA-C03 Study Guide** | Guia de estudo comunitário muito utilizado por candidatos à certificação | [🔗 Acessar](https://tutorialsdojo.com/aws-certified-solutions-architect-associate-saa-c03/) |
| 5 | **AWS FAQs – Core Services** | FAQs oficiais dos principais serviços: EC2, S3, RDS, VPC, IAM, Lambda | [🔗 Acessar](https://aws.amazon.com/faqs/) |

---

## 🧪 Engenharia de Prompts e Cicatrizes

Esta seção documenta as perguntas estratégicas elaboradas no NotebookLM, as variações testadas e as dificuldades encontradas no processo.

---

### Prompt 1 — Mapeamento dos Domínios

**Objetivo:** Entender o peso de cada domínio na prova.

**Prompt utilizado:**
```
Com base no Exam Guide SAA-C03, liste os 4 domínios da prova, seus respectivos pesos percentuais 
e os principais serviços AWS associados a cada domínio.
```

**Resposta obtida (resumo):**
O NotebookLM identificou corretamente os 4 domínios:
- **Domínio 1 – Design de Arquiteturas Seguras** (30%)
- **Domínio 2 – Design de Arquiteturas Resilientes** (26%)
- **Domínio 3 – Design de Arquiteturas de Alta Performance** (24%)
- **Domínio 4 – Design de Arquiteturas com Custo Otimizado** (20%)

**Dificuldades encontradas (cicatriz):**
A IA listou serviços muito genéricos inicialmente. Foi necessário refinar o prompt para obter serviços específicos por domínio.

**Prompt refinado:**
```
Para o Domínio 1 (Arquiteturas Seguras), quais são os 5 serviços AWS mais relevantes 
que um candidato precisa dominar? Explique brevemente o papel de cada um na segurança.
```

---

### Prompt 2 — Serviços Mais Cobrados

**Objetivo:** Priorizar o estudo nos serviços com maior frequência nas questões.

**Prompt utilizado:**
```
Quais são os 10 serviços AWS que mais aparecem nas questões da SAA-C03? 
Ordene por relevância e explique em uma frase o que cada um faz.
```

**Resposta obtida (resumo):**
Os serviços mais recorrentes identificados foram:
`EC2`, `S3`, `RDS`, `VPC`, `IAM`, `Lambda`, `CloudFront`, `Route 53`, `ELB/ALB`, `Auto Scaling`

**Dificuldades encontradas (cicatriz):**
O modelo confundiu ELB com ALB em alguns contextos. Foi necessário pedir uma diferenciação explícita entre os tipos de Load Balancer (ALB, NLB, CLB).

**Prompt refinado:**
```
Explique a diferença entre Application Load Balancer (ALB), Network Load Balancer (NLB) 
e Classic Load Balancer (CLB). Em qual cenário da SAA-C03 cada um seria a resposta correta?
```

---

### Prompt 3 — Cenários Arquiteturais

**Objetivo:** Treinar raciocínio para questões de cenário, que são o formato predominante na prova.

**Prompt utilizado:**
```
Crie 3 questões no estilo SAA-C03 envolvendo alta disponibilidade com EC2, RDS Multi-AZ 
e Auto Scaling. Inclua 4 alternativas e explique a resposta correta.
```

**Resposta obtida:** O NotebookLM gerou questões realistas com justificativa técnica para cada alternativa.

**Dificuldades encontradas (cicatriz):**
Algumas alternativas geradas eram muito parecidas entre si, o que não reflete bem o estilo real da prova. Adicionei instrução para incluir "distratores plausíveis mas incorretos".

**Prompt refinado:**
```
Nas 4 alternativas, inclua pelo menos 2 "distratores" — respostas que parecem corretas 
mas estão erradas por um detalhe técnico importante. Explique por que cada distrator está errado.
```

---

### Prompt 4 — Well-Architected Framework

**Objetivo:** Fixar os 6 pilares do Well-Architected Framework, muito cobrados na prova.

**Prompt utilizado:**
```
Resuma os 6 pilares do AWS Well-Architected Framework com exemplos práticos de serviços 
AWS que implementam cada pilar. Use linguagem técnica objetiva.
```

**Resposta obtida (resumo):**
Pilares identificados: Excelência Operacional, Segurança, Confiabilidade, Eficiência de Performance, Otimização de Custos e Sustentabilidade.

**Dificuldades encontradas (cicatriz):**
O pilar de **Sustentabilidade** foi adicionado em 2021 e nem todas as fontes o incluíam. O modelo inicialmente listou apenas 5 pilares, baseando-se em documentações mais antigas. Precisei referenciar explicitamente o whitepaper mais recente.

---

### Prompt 5 — Glossário Automatizado

**Objetivo:** Criar um glossário dos termos técnicos essenciais para revisão rápida.

**Prompt utilizado:**
```
Com base em todas as fontes carregadas, gere um glossário com os 20 termos técnicos AWS 
mais importantes para a SAA-C03. Formato: Termo | Definição em uma frase.
```

**Resultado:** Usado como base para o glossário na seção de Miniguia abaixo.

---

## 📖 Miniguia de Estudo — Entrega Final

---

### 1. Resumos Estruturados

#### 🔐 Domínio 1: Arquiteturas Seguras (30%)

Foco em **IAM**, **KMS**, **CloudTrail**, **Security Groups** e **NACLs**.

- **IAM**: Controle de acesso baseado em identidade. Sempre use o **princípio do menor privilégio**. Entenda a diferença entre Users, Groups, Roles e Policies.
- **Criptografia**: KMS gerencia chaves; S3 suporta SSE-S3, SSE-KMS e SSE-C. RDS pode ter criptografia em repouso habilitada na criação.
- **Rede Segura**: Security Groups são stateful (retorno automático); NACLs são stateless (precisam de regra de entrada e saída).
- **CloudTrail** registra chamadas de API; **CloudWatch** monitora métricas e logs.
- **VPN vs Direct Connect**: VPN é mais barato e rápido de configurar; Direct Connect oferece conexão dedicada e de baixa latência.

> 💡 **Dica de prova**: Quando a questão mencionar "auditoria" ou "quem fez o quê", a resposta quase sempre envolve **CloudTrail**.

---

#### 🔄 Domínio 2: Arquiteturas Resilientes (26%)

Foco em **Multi-AZ**, **Multi-Region**, **Auto Scaling**, **ELB** e **Route 53**.

- **Alta Disponibilidade**: RDS Multi-AZ faz failover automático para a réplica em outra AZ. Diferente de Read Replicas, que são para performance de leitura.
- **Auto Scaling**: Define capacidade mínima, desejada e máxima. Pode escalar por métricas (CPU, SQS) ou por agendamento.
- **Load Balancers**:
  - **ALB** (Application): Layer 7, roteamento por conteúdo (path/host-based). Ideal para microsserviços e containers.
  - **NLB** (Network): Layer 4, ultra baixa latência. Ideal para TCP/UDP e IPs elásticos.
  - **CLB** (Classic): Legado, evitar em projetos novos.
- **Route 53**: DNS com políticas de roteamento — Simple, Weighted, Latency-based, Failover, Geolocation, Geoproximity.

> 💡 **Dica de prova**: Se a questão fala em "roteamento de 20% do tráfego para nova versão", use **Weighted Routing** no Route 53.

---

#### ⚡ Domínio 3: Alta Performance (24%)

Foco em **S3**, **ElastiCache**, **CloudFront**, **SQS/SNS** e **Kinesis**.

- **S3**: Storage classes — Standard, Intelligent-Tiering, Standard-IA, One Zone-IA, Glacier, Glacier Deep Archive. Use **Lifecycle Policies** para automatizar transições.
- **Cache**: ElastiCache (Redis/Memcached) reduz latência de banco de dados. Redis suporta persistência e estruturas de dados avançadas.
- **CDN**: CloudFront distribui conteúdo globalmente via edge locations. Suporta HTTPS, signed URLs e signed cookies.
- **Filas e Streaming**:
  - **SQS**: Fila gerenciada. Standard (at-least-once) vs FIFO (exatamente uma vez, em ordem).
  - **SNS**: Pub/Sub. Notificações para múltiplos consumidores simultaneamente.
  - **Kinesis**: Streaming de dados em tempo real. Data Streams (processamento) vs Firehose (entrega a S3/Redshift).

> 💡 **Dica de prova**: "Desacoplar componentes" → **SQS**. "Notificar múltiplos sistemas ao mesmo tempo" → **SNS**.

---

#### 💰 Domínio 4: Custo Otimizado (20%)

Foco em modelos de preço EC2, **S3 Intelligent-Tiering**, **Spot Instances** e **AWS Cost Explorer**.

- **Modelos EC2**: On-Demand (flexibilidade), Reserved (desconto 1-3 anos), Spot (até 90% mais barato, interruptível), Dedicated Hosts (compliance).
- **Serverless**: Lambda elimina custo de servidor ocioso. Cobrado por execução e duração.
- **Armazenamento**: S3 Intelligent-Tiering move dados automaticamente entre tiers de custo. Glacier para dados raramente acessados.
- **Rightsizing**: Use AWS Compute Optimizer para recomendações de instâncias mais eficientes.

> 💡 **Dica de prova**: Workloads tolerantes a interrupção (batch jobs, CI/CD) → **Spot Instances**.

---

### 2. Glossário de Conceitos

| Termo | Definição |
|-------|-----------|
| **AZ (Availability Zone)** | Data center isolado dentro de uma Região AWS com energia e rede independentes |
| **Region** | Área geográfica com múltiplas AZs interconectadas por fibra de baixa latência |
| **VPC (Virtual Private Cloud)** | Rede virtual isolada dentro da AWS onde você controla IPs, rotas e gateways |
| **IAM Role** | Conjunto de permissões que pode ser assumido por serviços ou usuários temporariamente |
| **Security Group** | Firewall stateful a nível de instância; controla tráfego de entrada e saída |
| **NACL** | Firewall stateless a nível de subnet; avalia regras de entrada e saída separadamente |
| **ELB** | Elastic Load Balancer; distribui tráfego automaticamente entre múltiplos alvos |
| **AMI** | Amazon Machine Image; template para criar instâncias EC2 com OS e configurações |
| **S3 Bucket** | Contêiner de armazenamento de objetos com capacidade virtualmente ilimitada |
| **RDS Multi-AZ** | Configuração com réplica síncrona em outra AZ para failover automático |
| **Read Replica** | Cópia assíncrona de banco de dados para escalar leituras (não serve como failover) |
| **Auto Scaling Group** | Conjunto de EC2 que escala automaticamente com base em políticas definidas |
| **CloudFront** | CDN da AWS que distribui conteúdo via edge locations ao redor do mundo |
| **Route 53** | Serviço DNS gerenciado com roteamento inteligente e health checks |
| **Lambda** | Serviço serverless que executa código em resposta a eventos sem provisionar servidores |
| **SQS** | Serviço de filas gerenciadas para desacoplar componentes de aplicações |
| **SNS** | Serviço pub/sub para envio de notificações a múltiplos assinantes |
| **Kinesis** | Plataforma para ingestão e processamento de dados de streaming em tempo real |
| **CloudTrail** | Serviço de auditoria que registra todas as chamadas de API feitas na conta AWS |
| **KMS** | Serviço de gerenciamento de chaves criptográficas com integração nativa AWS |
| **ElastiCache** | Serviço gerenciado de cache em memória (Redis e Memcached) |
| **Well-Architected** | Framework com 6 pilares para avaliar e melhorar arquiteturas na AWS |
| **Spot Instance** | Capacidade EC2 ociosa com desconto de até 90%, podendo ser interrompida pela AWS |
| **Reserved Instance** | Compromisso de 1 ou 3 anos com EC2 em troca de desconto significativo |

---

### 3. Prompts Reutilizáveis para Revisão

Estes prompts podem ser usados em futuras sessões no NotebookLM ou em qualquer LLM para revisão do conteúdo.

```
📌 PROMPT 1 — REVISÃO DE SERVIÇO
"Explique o serviço [NOME DO SERVIÇO] no contexto da SAA-C03:
(1) O que ele faz em uma frase;
(2) Casos de uso típicos na prova;
(3) Diferença do serviço mais parecido;
(4) Armadilha mais comum nas questões."
```

```
📌 PROMPT 2 — CRIAÇÃO DE QUESTÕES DE PROVA
"Crie 5 questões no estilo SAA-C03 sobre [TEMA].
- 4 alternativas por questão
- Pelo menos 2 distratores plausíveis
- Gabarito comentado ao final
- Identifique a qual domínio da prova cada questão pertence."
```

```
📌 PROMPT 3 — COMPARAÇÃO DE SERVIÇOS
"Compare [SERVIÇO A] e [SERVIÇO B] em formato de tabela com as colunas:
Característica | Serviço A | Serviço B.
Inclua: tipo de dado, latência, durabilidade, caso de uso ideal e quando NÃO usar cada um."
```

```
📌 PROMPT 4 — REVISÃO DE CENÁRIO ARQUITETURAL
"Dado o cenário: [DESCREVA O CENÁRIO].
Qual seria a arquitetura AWS ideal? Justifique a escolha de cada serviço 
com base nos pilares do Well-Architected Framework."
```

```
📌 PROMPT 5 — FLASHCARD DE REVISÃO RÁPIDA
"Para o tópico [TEMA], crie 10 flashcards no formato:
FRENTE: [pergunta objetiva]
VERSO: [resposta em até 2 linhas]
Foque nos pontos que mais caem na SAA-C03."
```

```
📌 PROMPT 6 — DIAGNÓSTICO DE PONTOS FRACOS
"Com base nas fontes carregadas, quais são os 5 tópicos da SAA-C03 
que os candidatos mais erram? Para cada um, explique:
(1) Por que é difícil;
(2) Qual a pegadinha comum;
(3) Como fixar o conceito corretamente."
```

---

## 🗺️ Roadmap de Estudos Sugerido

```
Semana 1: Domínio 1 (Segurança) → IAM, VPC, KMS, CloudTrail
Semana 2: Domínio 2 (Resiliência) → EC2, RDS, ELB, Auto Scaling, Route 53
Semana 3: Domínio 3 (Performance) → S3, ElastiCache, CloudFront, SQS/SNS, Kinesis
Semana 4: Domínio 4 (Custos) → Modelos de preço, Lambda, Serverless, Cost Explorer
Semana 5: Simulados e revisão geral (mínimo 3 simulados completos)
```

> 🎯 **Meta de score**: Acima de 80% nos simulados antes de agendar a prova real (passing score oficial: 720/1000).

---

## 🔧 Ferramentas Utilizadas

- **[NotebookLM](https://notebooklm.google.com/)** — Curadoria e análise das fontes, geração do caderno temático
- **GitHub** — Repositório e documentação do projeto
- **[Tutorials Dojo](https://tutorialsdojo.com/)** — Simulados e cheat sheets
- **[AWS Skill Builder](https://skillbuilder.aws/)** — Cursos oficiais gratuitos

---

## 📬 Sobre o Projeto

Este repositório foi criado como entrega do **Desafio de Projeto da DIO** com o tema de exploração do NotebookLM como ferramenta de aprendizagem ativa. O conteúdo foi produzido com auxílio de IA e curadoria manual, refletindo um processo real de estudo para a certificação AWS Solutions Architect Associate.

---

*Feito com ☁️ e dedicação para a comunidade DIO.*

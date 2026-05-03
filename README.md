# 🧩 Miniguia de Estudos: Microsserviços com Spring Boot

> Caderno temático criado com auxílio do NotebookLM como parte do desafio prático da [DIO](https://www.dio.me/) — explorando IA como ferramenta ativa de aprendizagem.

---

## 📋 Sumário

- [Contexto e Objetivos](#-contexto-e-objetivos)
- [Curadoria de Fontes](#-curadoria-de-fontes)
- [Engenharia de Prompts e Cicatrizes](#-engenharia-de-prompts-e-cicatrizes)
- [Miniguia de Estudo](#-miniguia-de-estudo-entrega-final)
  - [Resumos Estruturados](#resumos-estruturados)
  - [Glossário](#glossário)
  - [Prompts Reutilizáveis](#prompts-reutilizáveis)

---

## 🎯 Contexto e Objetivos

### Contexto

Este repositório documenta minha jornada de estudo sobre **Arquitetura de Microsserviços com Spring Boot**, utilizando o [NotebookLM](https://notebooklm.google.com/) do Google como ferramenta central de curadoria, síntese e geração de conhecimento.

O tema foi escolhido por ser diretamente aplicado ao meu portfólio técnico: tenho trabalhado com Java/Spring Boot e quero consolidar fundamentos sólidos de arquitetura distribuída para me posicionar melhor no mercado como desenvolvedor back-end júnior.

### Objetivos de Estudo

| # | Objetivo | Status |
|---|----------|--------|
| 1 | Compreender os princípios fundamentais da arquitetura de microsserviços | ✅ |
| 2 | Entender como o Spring Boot facilita a criação de serviços independentes | ✅ |
| 3 | Aprender sobre comunicação entre serviços (REST, mensageria) | ✅ |
| 4 | Explorar padrões como API Gateway, Service Discovery e Circuit Breaker | ✅ |
| 5 | Entender o papel de ferramentas como Docker e Kubernetes no ecossistema | ✅ |
| 6 | Criar um conjunto de prompts reutilizáveis para revisão futura | ✅ |

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas com critério: priorizei materiais gratuitos, em inglês ou português, com boa densidade técnica e didática. Todas foram enviadas ao NotebookLM para análise cruzada.

### Fonte 1 — Documentação Oficial do Spring
**Título:** Spring Boot Reference Documentation  
**Link:** [https://docs.spring.io/spring-boot/docs/current/reference/html/](https://docs.spring.io/spring-boot/docs/current/reference/html/)  
**Formato:** HTML / PDF  
**Por que escolhi:** Fonte primária e mais confiável sobre o framework. Cobre desde auto-configuração até produção com Actuator e métricas.

---

### Fonte 2 — Guia da Red Hat sobre Microsserviços
**Título:** What are microservices? — Red Hat  
**Link:** [https://www.redhat.com/en/topics/microservices/what-are-microservices](https://www.redhat.com/en/topics/microservices/what-are-microservices)  
**Formato:** Artigo Web  
**Por que escolhi:** Explica o conceito de forma clara, comparando com arquitetura monolítica, sem ser superficial. Ótimo ponto de entrada.

---

### Fonte 3 — Artigo de Martin Fowler sobre Microsserviços
**Título:** Microservices — a definition of this new architectural term  
**Link:** [https://martinfowler.com/articles/microservices.html](https://martinfowler.com/articles/microservices.html)  
**Formato:** Artigo Web / PDF  
**Por que escolhi:** Considerado o artigo "canônico" sobre microsserviços. Martin Fowler define os princípios que todo desenvolvedor sério precisa conhecer.

---

### Fonte 4 — Baeldung: Microsserviços com Spring Cloud
**Título:** Microservices with Spring Cloud  
**Link:** [https://www.baeldung.com/spring-cloud-series](https://www.baeldung.com/spring-cloud-series)  
**Formato:** Série de artigos técnicos  
**Por que escolhi:** O Baeldung é referência prática para o ecossistema Spring. Esta série cobre Eureka, Feign, Zuul/Gateway e Config Server com exemplos de código reais.

---

### Fonte 5 — Livro Gratuito: Designing Distributed Systems (O'Reilly)
**Título:** Designing Distributed Systems — Patterns and Paradigms  
**Link:** [https://azure.microsoft.com/en-us/resources/designing-distributed-systems/](https://azure.microsoft.com/en-us/resources/designing-distributed-systems/)  
**Formato:** PDF Gratuito  
**Por que escolhi:** Traz padrões de design para sistemas distribuídos com exemplos práticos em containers. Complementa perfeitamente a parte teórica dos outros materiais.

---

## 🔬 Engenharia de Prompts e Cicatrizes

Esta seção documenta o processo de interação com o NotebookLM: os prompts testados, as respostas obtidas, os ajustes realizados e as dificuldades encontradas. É aqui que o aprendizado real aparece.

---

### 🧪 Experimento 1 — Entendendo a diferença entre Monolito e Microsserviços

**Prompt inicial (v1):**
> "Explique microsserviços."

**Problema encontrado:**  
A resposta foi genérica demais. O NotebookLM resumiu as fontes sem aprofundamento, misturando conceitos sem conectá-los.

**Prompt refinado (v2):**
> "Com base nas fontes carregadas, quais são as principais diferenças entre arquitetura monolítica e arquitetura de microsserviços? Cite vantagens e desvantagens de cada abordagem com exemplos práticos."

**Resultado:**  
Muito melhor. A IA cruzou o artigo do Fowler com o da Red Hat e apresentou um comparativo claro, com referências explícitas nas fontes.

**🔑 Lição aprendida:** Prompts vagos geram respostas vagas. Especificar o *tipo de saída esperada* (comparativo, lista, explicação com exemplos) faz toda a diferença.

---

### 🧪 Experimento 2 — Padrões de Microsserviços

**Prompt (v1):**
> "Quais são os padrões de design mais importantes para microsserviços?"

**Problema encontrado:**  
O NotebookLM listou os padrões, mas não explicou *quando usar cada um*. A resposta era correta mas inaplicável na prática.

**Prompt refinado (v2):**
> "Dentre os padrões de microsserviços mencionados nas fontes (API Gateway, Circuit Breaker, Service Discovery, Sidecar, Saga), explique o problema que cada um resolve e quando é recomendado aplicá-lo. Dê um exemplo de cenário real para cada."

**Resultado:**  
Excelente. A IA trouxe o Circuit Breaker ligado ao problema de falha em cascata, o API Gateway como solução para acoplamento de clientes, e o Saga para consistência eventual em transações distribuídas, tudo com referências às fontes.

**🔑 Lição aprendida:** Ao listar os conceitos no próprio prompt, você guia a IA a cobrí-los todos, sem lacunas.

---

### 🧪 Experimento 3 — Spring Cloud na prática

**Prompt (v1):**
> "Como usar Spring Cloud?"

**Problema encontrado:**  
Resposta muito longa e sem foco. A IA tentou cobrir toda a documentação do Spring Cloud de uma vez.

**Prompt refinado (v2):**
> "Focando na fonte do Baeldung sobre Spring Cloud, explique o papel de cada componente abaixo e como eles se comunicam numa arquitetura típica de microsserviços: (1) Eureka Server, (2) Spring Cloud Gateway, (3) OpenFeign, (4) Config Server."

**Resultado:**  
A IA gerou um fluxo coeso explicando como o Eureka faz o registro, o Gateway roteia as requisições, o Feign abstrai chamadas HTTP entre serviços e o Config Server centraliza configurações — tudo conectado.

**⚠️ Dificuldade encontrada (cicatriz):** O NotebookLM às vezes confunde versões do Spring Cloud (Bootstrap vs. a abordagem moderna com `spring-config-import`). Foi necessário formular um novo prompt:
> "A explicação acima usa a abordagem com `bootstrap.yml`. Como isso muda na versão moderna com Spring Boot 2.4+?"

**🔑 Lição aprendida:** Quando suspeitar de informações desatualizadas, faça perguntas de follow-up específicas sobre versões.

---

### 🧪 Experimento 4 — Docker e Kubernetes no contexto de Microsserviços

**Prompt:**
> "Com base nas fontes disponíveis, como Docker e Kubernetes se encaixam na infraestrutura de microsserviços? Qual é a responsabilidade de cada um e como eles se complementam?"

**Resultado:**  
Boa resposta. A IA diferenciou claramente Docker como ferramenta de empacotamento/isolamento e Kubernetes como orquestrador. Mencionou conceitos como Pods, Services e Deployments.

**⚠️ Dificuldade encontrada (cicatriz):** O livro da O'Reilly tem foco em sistemas distribuídos genéricos, não especificamente em microsserviços com Java. A IA tentou aplicar os exemplos em Go do livro para o contexto Spring, o que gerou confusão.

**Correção aplicada:**
> "Ignore os exemplos de código do livro da O'Reilly e foque apenas nos conceitos arquiteturais. Como esses conceitos se aplicam a um ambiente Spring Boot com múltiplos serviços?"

**🔑 Lição aprendida:** É possível instruir o NotebookLM a *ignorar partes* de uma fonte e focar em aspectos específicos.

---

### 🧪 Experimento 5 — Geração do Glossário

**Prompt:**
> "Com base em todas as fontes carregadas, gere um glossário com os 20 termos técnicos mais importantes do universo de microsserviços com Spring Boot. Para cada termo, inclua: (1) definição concisa, (2) contexto de uso, (3) a fonte onde o conceito aparece com mais clareza."

**Resultado:**  
Este foi o prompt mais produtivo de toda a sessão. O glossário gerado foi denso e bem referenciado. Serviu de base para a seção de glossário deste README.

**🔑 Lição aprendida:** Para geração de material de referência (glossários, cheat sheets), peça ao NotebookLM para estruturar a resposta num formato fixo com campos definidos, o resultado é muito mais utilizável.

---

## 📖 Miniguia de Estudo (Entrega Final)

---

### Resumos Estruturados

#### 📌 Módulo 1 — O que são Microsserviços?

Microsserviços são uma abordagem arquitetural onde uma aplicação é decomposta em **serviços pequenos, independentes e implantáveis separadamente**. Cada serviço é responsável por um domínio de negócio específico e se comunica com outros via APIs bem definidas (geralmente REST ou mensageria assíncrona).

**Características fundamentais:**
- **Componentização via serviços:** cada parte do sistema vive em seu próprio processo
- **Organização em torno de capacidades de negócio:** times multifuncionais donos de seus serviços
- **Implantação independente:** atualizar um serviço não exige reimplantar o sistema todo
- **Descentralização de dados:** cada microsserviço tem seu próprio banco de dados
- **Tolerância a falhas:** o sistema é projetado para lidar com falhas parciais

**Quando NÃO usar microsserviços:**
- Em projetos pequenos ou times reduzidos (overhead operacional é alto)
- Quando a fronteira entre domínios ainda não está clara
- Quando a equipe não tem maturidade em DevOps/containers

---

#### 📌 Módulo 2 — Spring Boot como Base dos Serviços

O Spring Boot é a escolha dominante no ecossistema Java para construção de microsserviços por conta de:

- **Auto-configuração:** elimina XML e reduz boilerplate
- **Servidor embutido:** cada serviço sobe como um JAR standalone (Tomcat/Netty embedded)
- **Spring Actuator:** endpoints de health check, métricas e monitoramento prontos
- **Ecossistema Spring Cloud:** extensões prontas para todos os padrões de microsserviços

**Estrutura típica de um microsserviço Spring Boot:**

```
meu-servico/
├── src/main/java/
│   └── com/empresa/meuservico/
│       ├── MeuServicoApplication.java    # Entry point
│       ├── controller/                   # REST controllers
│       ├── service/                      # Regras de negócio
│       ├── repository/                   # Acesso a dados (JPA/Mongo)
│       └── dto/                          # Data Transfer Objects
├── src/main/resources/
│   └── application.yml                   # Configurações
└── Dockerfile                            # Container definition
```

---

#### 📌 Módulo 3 — Comunicação entre Serviços

Existem dois paradigmas principais de comunicação:

**Síncrona (REST/HTTP):**
- Uso do Spring Web com `RestTemplate` ou `WebClient`
- Com Spring Cloud: **OpenFeign** (cliente declarativo)
- Simples, mas cria acoplamento temporal (serviço A depende de B estar UP)

```java
// Exemplo com OpenFeign
@FeignClient(name = "pedido-service")
public interface PedidoClient {
    @GetMapping("/pedidos/{id}")
    PedidoDTO buscarPedido(@PathVariable Long id);
}
```

**Assíncrona (Mensageria):**
- **RabbitMQ** com Spring AMQP
- **Apache Kafka** com Spring Kafka
- Desacopla serviços temporalmente: produtor não precisa que consumidor esteja disponível

```java
// Exemplo com RabbitMQ
@RabbitListener(queues = "pedidos.criados")
public void processarPedido(PedidoDTO pedido) {
    // processar evento
}
```

---

#### 📌 Módulo 4 — Padrões Essenciais com Spring Cloud

| Padrão | Problema que resolve | Solução Spring Cloud |
|--------|---------------------|----------------------|
| **Service Discovery** | Como serviços se encontram sem IPs fixos | Eureka Server + Eureka Client |
| **API Gateway** | Ponto único de entrada para clientes externos | Spring Cloud Gateway |
| **Circuit Breaker** | Evita falha em cascata quando um serviço cai | Resilience4j |
| **Config Server** | Centralizar configurações de todos os serviços | Spring Cloud Config |
| **Load Balancing** | Distribuir carga entre instâncias | Spring Cloud LoadBalancer |
| **Distributed Tracing** | Rastrear requisições entre serviços | Micrometer + Zipkin |

---

#### 📌 Módulo 5 — Docker e Orquestração

**Docker** empacota cada microsserviço em um container isolado:

```dockerfile
# Dockerfile típico para Spring Boot
FROM eclipse-temurin:21-jre-alpine
WORKDIR /app
COPY target/meu-servico.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]
```

**Docker Compose** para desenvolvimento local com múltiplos serviços:

```yaml
services:
  eureka-server:
    build: ./eureka-server
    ports: ["8761:8761"]

  pedido-service:
    build: ./pedido-service
    ports: ["8081:8081"]
    depends_on: [eureka-server, postgres]
    environment:
      EUREKA_URI: http://eureka-server:8761/eureka

  postgres:
    image: postgres:16-alpine
    environment:
      POSTGRES_DB: pedidos
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
```

**Kubernetes** em produção: garante alta disponibilidade, auto-scaling e self-healing dos containers.

---

### Glossário

> Termos essenciais do universo de Microsserviços com Spring Boot, em ordem alfabética.

| Termo | Definição |
|-------|-----------|
| **API Gateway** | Ponto único de entrada que roteia requisições externas para os microsserviços corretos. Pode fazer autenticação, rate limiting e transformação de payloads. |
| **Auto-configuração** | Mecanismo do Spring Boot que detecta dependências no classpath e configura beans automaticamente, sem necessidade de XML. |
| **Circuit Breaker** | Padrão que "abre o circuito" (para de chamar) um serviço com falhas repetidas, evitando cascata de erros. Implementado com Resilience4j no ecossistema Spring. |
| **Config Server** | Servidor centralizado (Spring Cloud Config) que fornece propriedades de configuração para todos os microsserviços via Git ou sistema de arquivos. |
| **Container** | Unidade de software que empacota código + dependências + runtime, garantindo execução consistente em qualquer ambiente. Gerenciado pelo Docker. |
| **Docker Compose** | Ferramenta para definir e executar aplicações multi-container com um único arquivo YAML. Essencial para dev local com microsserviços. |
| **Domínio (DDD)** | Área de conhecimento ou negócio. Em microsserviços, cada serviço é idealmente responsável por um único domínio de negócio. |
| **Eureka** | Servidor de registro de serviços (Service Registry) do Netflix OSS, integrado ao Spring Cloud. Permite que serviços se registrem e descubram uns aos outros dinamicamente. |
| **Failover** | Mecanismo de tolerância a falhas que redireciona tráfego automaticamente para uma instância saudável quando outra falha. |
| **Feign (OpenFeign)** | Cliente HTTP declarativo integrado ao Spring Cloud. Permite chamar outros serviços como se fossem interfaces Java simples. |
| **Health Check** | Endpoint (geralmente `/actuator/health`) que informa o estado de saúde de um serviço. Usado pelo orquestrador para detectar instâncias falhas. |
| **Idempotência** | Propriedade de uma operação que pode ser executada múltiplas vezes sem alterar o resultado além da primeira execução. Essencial em sistemas distribuídos. |
| **Kubernetes (K8s)** | Plataforma de orquestração de containers que automatiza deploy, scaling e gerenciamento de aplicações containerizadas em produção. |
| **Load Balancer** | Distribui o tráfego de entrada entre múltiplas instâncias de um serviço para evitar sobrecarga. No Spring Cloud, é feito client-side via Spring Cloud LoadBalancer. |
| **Mensageria** | Padrão de comunicação assíncrona entre serviços via troca de mensagens (eventos). Principais brokers: RabbitMQ e Apache Kafka. |
| **Microsserviço** | Serviço pequeno, independente e de responsabilidade única, deployável isoladamente, que se comunica via APIs. |
| **Monolito** | Aplicação onde todos os componentes (UI, negócio, dados) estão num único processo deployável. Oposto de microsserviços. |
| **Pod** | Menor unidade implantável no Kubernetes. Contém um ou mais containers que compartilham rede e armazenamento. |
| **Resiliência** | Capacidade de um sistema de continuar funcionando (mesmo que degradado) quando partes falham. |
| **Saga Pattern** | Padrão para gerenciar transações distribuídas em microsserviços via sequência de transações locais com eventos compensatórios em caso de falha. |
| **Service Discovery** | Mecanismo que permite que microsserviços se encontrem dinamicamente, sem depender de IPs/portas fixos. |
| **Service Mesh** | Camada de infraestrutura que gerencia comunicação service-to-service (ex: Istio). Delega lógica de resiliência para a infraestrutura. |
| **Spring Actuator** | Módulo do Spring Boot que expõe endpoints de gerenciamento: health, metrics, info, env, etc. |
| **Spring Cloud** | Conjunto de ferramentas que estendem o Spring Boot com padrões para sistemas distribuídos: Config, Gateway, Eureka, Feign, etc. |
| **Tolerância a Falhas** | Capacidade do sistema de continuar operando mesmo quando componentes individuais falham. Implementada via Circuit Breaker, Retry, Bulkhead. |

---

### Prompts Reutilizáveis

> Coleção de prompts validados para usar em futuras sessões de revisão no NotebookLM ou com qualquer LLM.

---

#### 🔁 Para revisão conceitual

```
Com base nas fontes sobre microsserviços, explique [CONCEITO] de forma clara:
1. O que é
2. Qual problema ele resolve
3. Quando usar e quando NÃO usar
4. Exemplo prático com Spring Boot
```

---

#### 🔁 Para comparações técnicas

```
Compare [TECNOLOGIA A] e [TECNOLOGIA B] no contexto de microsserviços com Spring Boot:
- Caso de uso ideal de cada uma
- Trade-offs (vantagens e desvantagens)
- Qual escolher para um projeto [pequeno/médio/grande escala]
```

---

#### 🔁 Para entender padrões de design

```
Explique o padrão [NOME DO PADRÃO] em microsserviços:
1. Contexto: qual problema surge sem esse padrão?
2. Solução: como o padrão resolve o problema?
3. Implementação: como fazer com Spring Boot/Spring Cloud?
4. Cuidados: quais são os riscos ou limitações?
```

---

#### 🔁 Para gerar exemplos de código

```
Gere um exemplo mínimo e funcional em Spring Boot que demonstre [CONCEITO/PADRÃO].
O código deve:
- Ser autocontido (pode ser um único arquivo ou projeto mínimo)
- Incluir comentários explicando cada parte importante
- Usar boas práticas modernas (Spring Boot 3.x, Java 21)
```

---

#### 🔁 Para troubleshooting de conceitos

```
Estou confuso sobre a diferença entre [CONCEITO A] e [CONCEITO B].
Explique como se eu fosse um desenvolvedor júnior, usando uma analogia do mundo real
e depois um exemplo técnico em Spring Boot.
```

---

#### 🔁 Para revisar antes de entrevistas

```
Gere 10 perguntas de entrevista técnica sobre [TEMA] no nível [júnior/pleno/sênior],
com as respostas esperadas de um candidato bem preparado.
Inclua pelo menos 2 perguntas práticas ("Como você implementaria...").
```

---

#### 🔁 Para criar resumos de novos conteúdos

```
Leia o conteúdo abaixo e gere:
1. Um resumo de 5 linhas (visão geral)
2. Os 5 pontos mais importantes (bullet points)
3. 3 perguntas de estudo para testar compreensão
4. Conexão com o que já sei sobre microsserviços com Spring Boot

[COLAR CONTEÚDO AQUI]
```

---

## 🛠️ Stack Utilizada no Portfólio

As tecnologias estudadas neste caderno temático aplicadas no projeto de portfólio:

![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Spring Cloud](https://img.shields.io/badge/Spring_Cloud-2023.x-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)

---

## 📊 Reflexão Final

| Aspecto | Avaliação |
|---------|-----------|
| **Qualidade das fontes** | Fontes primárias + artigos de referência formaram uma base sólida |
| **NotebookLM como ferramenta** | Excelente para síntese cruzada; requer prompts bem formulados |
| **Principal aprendizado técnico** | Entender que microsserviços não são bala de prata — o custo operacional é real |
| **Principal aprendizado de prompt** | Especificidade > Generalidade. Prompts com estrutura definida geram resultados utilizáveis |

---

## 🔗 Links Úteis

- [Spring Initializr](https://start.spring.io/) — Gerador de projetos Spring Boot
- [Spring Cloud Documentation](https://spring.io/projects/spring-cloud)
- [Resilience4j Docs](https://resilience4j.readme.io/)
- [Docker Hub — Imagens Oficiais](https://hub.docker.com/)
- [12 Factor App](https://12factor.net/pt_br/) — Metodologia para apps cloud-native

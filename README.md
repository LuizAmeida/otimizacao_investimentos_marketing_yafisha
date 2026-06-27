# Otimização de Investimentos de Marketing - Y.Afisha

> Projeto de análise de dados de uma plataforma de entretenimento (Y.Afisha) para otimizar despesas com publicidade, avaliando o comportamento dos usuários, métricas de vendas e performance de canais de marketing.

---

## 🎯 Objetivo do Projeto

Analisar dados de acessos, pedidos e custos de marketing para responder a perguntas fundamentais de crescimento (Growth):

1. **Produto:** Como os usuários interagem com a plataforma e qual a taxa de retenção?
2. **Vendas:** Qual o tempo médio de conversão e o valor gerado por cada cliente (LTV)?
3. **Marketing:** Quais origens de anúncio são rentáveis e quais apresentam custo de aquisição inviável (CAC)?

---

## 📊 Resultados Obtidos

### 1. Análise do Produto (Comportamento dos Usuários)

| Métrica | Valor |
|---------|-------|
| DAU médio | 908 usuários/dia |
| WAU médio | 4.573 usuários/semana |
| MAU médio | 12.371 usuários/mês |
| Média de sessões por dia | 982,5 |
| Média de sessões por usuário/dia | 1,08 |
| Duração média da sessão | 9,5 minutos |
| Duração mediana da sessão | 6,0 minutos |
| Retenção D1 | 2,6% |
| Usuários que voltaram | 22,8% |

**Principais descobertas:**
- Usuários raramente acessam mais de uma vez por dia (média de 1,08 sessões)
- Sessões são curtas e objetivas (mediana de 6 minutos)
- **Retenção crítica:** apenas 2,6% dos usuários retornam no dia seguinte
- 77,2% dos usuários nunca retornam após a primeira visita

---

### 2. Análise de Vendas

| Métrica | Valor |
|---------|-------|
| Tempo médio para conversão | 0,8 dias |
| Mediana para conversão | 0 dias |
| **Conversão no mesmo dia (D0)** | **72,2%** |
| Conversão em 1-7 dias | 15,8% |
| Conversão em 8-30 dias | 8,1% |
| Conversão em 30+ dias | 3,9% |
| Média de pedidos por cliente | 1,35 |
| Clientes recorrentes (2+ pedidos) | 26,2% |
| **Ticket médio geral** | **R$ 5,00** |
| Ticket médio - Desktop | R$ 5,17 |
| Ticket médio - Touch | R$ 4,26 |
| **LTV médio** | **R$ 6,79** |

**Principais descobertas:**
- **72,2%** das compras ocorrem no mesmo dia da primeira visita (comportamento de compra imediata)
- Ticket médio baixo (R$ 5,00) com tendência de queda ao longo de 2018
- Usuários de **Desktop** são mais valiosos (ticket 17% maior que Touch)
- LTV máximo ocorre no mês 0 (primeira compra), caindo rapidamente nos meses seguintes

---

### 3. Análise de Marketing

#### Resumo por Origem (Ordenado por ROI)

| Source ID | Investimento (R$) | Clientes | Receita (R$) | CAC (R$) | ROI (%) | Conversão (%) |
|-----------|-------------------|----------|--------------|----------|---------|---------------|
| **1** | 28.540,14 | 3.972 | 42.592,93 | 7,19 | **49,24** | 15,2 |
| **2** | 19.558,84 | 2.841 | 21.440,37 | 6,88 | **9,62** | 11,8 |
| **5** | 10.042,42 | 1.462 | 10.916,91 | 6,87 | **8,71** | 10,9 |
| **9** | 27.870,75 | 5.499 | 30.148,45 | 5,07 | **8,17** | 9,1 |
| **10** | 5.224,58 | 1.192 | 4.876,92 | 4,38 | **-6,65** | 6,7 |
| **4** | 61.073,60 | 5.653 | 56.696,83 | 10,80 | **-7,17** | 10,4 |
| **8** | 8.062,42 | 771 | 5.411,54 | 10,46 | **-32,88** | 12,3 |
| **7** | 8.892,99 | 896 | 5.890,31 | 9,93 | **-33,77** | 11,9 |
| **6** | 18.454,75 | 1.556 | 9.678,92 | 11,86 | **-47,55** | 10,8 |
| **3** | 141.321,63 | 10.476 | 54.524,42 | 13,49 | **-61,43** | 9,2 |

---

#### Resumo de Marketing

| Métrica | Valor |
|---------|-------|
| **Investimento total** | **R$ 329.131,62** |
| **Canais com ROI positivo** | **4 origens** (1, 2, 5, 9) |
| **Canais com ROI negativo** | **6 origens** (3, 4, 6, 7, 8, 10) |
| **Melhor canal (ROI)** | **Origem 1** (49,24%) |
| **Pior canal (ROI)** | **Origem 3** (-61,43%) |
| **Menor CAC** | Origem 10 (R$ 4,38) |
| **Maior investimento** | Origem 3 (R$ 141.321,63 - 43% do total) |

**Principais descobertas:**
- **Origem 3** é o maior problema: 43% do orçamento, maior CAC e pior ROI
- **Origem 1** é o melhor canal: ROI de 49,24% e CAC de R$ 7,19
- Canais com ROI positivo receberam apenas **28,6%** do investimento
- Canais com ROI negativo receberam **71,4%** do investimento
- **R$ 202.395,23** (62% do orçamento) foi investido em canais com ROI negativo

---

### 4. Teste de Hipótese: Comparação de LTV por Dispositivo

**Hipótese:** O LTV (Lifetime Value) é maior para usuários de Desktop em comparação com usuários de Touch.

**Resultado:** Confirmado. Desktop apresenta LTV 14,9% maior que Touch.

---

## 🛠️ Ferramentas Utilizadas

- **Python 3**
- **Bibliotecas:**
  - `pandas` — manipulação e análise de dados
  - `numpy` — operações matemáticas
  - `matplotlib` — visualização de dados
  - `seaborn` — visualização estatística
  - `scipy.stats` — testes estatísticos

---

## 📚 O que Aprendi

- **Análise de produto:** cálculo de DAU, WAU, MAU, retenção e duração de sessões
- **Análise de vendas:** tempo de conversão, ticket médio, LTV e análise de coortes
- **Análise de marketing:** CAC, ROI, ROMI e avaliação de canais de aquisição
- **Análise de coortes:** acompanhamento do LTV ao longo do tempo
- **Visualização de dados:** gráficos de barras, boxplots, heatmaps e séries temporais
- **Tomada de decisão baseada em dados:** recomendações de alocação de orçamento

---

## 🚀 Como Executar o Projeto

```bash
# Clone o repositório
git clone https://github.com/LuizAlmeida/otimizacao_investimentos_marketing_yafisha

# Navegue até a pasta do projeto
cd otimizacao_investimentos_marketing_yafisha

# Execute o notebook (recomendado: Google Colab ou Jupyter Notebook)
````

## Requisitos:
- Python 3.x instalado
- Jupyter Notebook (opcional) ou Google Colab (recomendado)
- Bibliotecas: pip install pandas numpy matplotlib seaborn scipy


## 🔍 Metodologia
O projeto seguiu uma abordagem estruturada em 6 etapas:


## Etapa 1: Carregamento e Preparação dos Dados
- Leitura dos 3 arquivos CSV (visits, orders, costs)
- Conversão de tipos de dados para datetime
- Padronização de nomes de colunas

## Etapa 2: Análise do Produto
- Cálculo de DAU, WAU, MAU
- Análise de sessões por dia
- Distribuição da duração das sessões
- Cálculo da retenção de usuários (D1)

## Etapa 3: Análise de Vendas
- Tempo até a primeira compra (conversão)
- Número de pedidos por cliente
- Ticket médio por dispositivo e mês
- Cálculo do LTV (Lifetime Value) por coorte

## Etapa 4: Análise de Marketing
- Cálculo de gastos totais e por origem
- Cálculo do CAC (Custo de Aquisição) por origem
- Cálculo do ROI e ROMI por origem
- Análise de performance por canal

## Etapa 5: Visualizações
- Evolução do DAU
- Comparação de usuários vs sessões
- Distribuição da duração das sessões
- Gastos, CAC e ROI por origem
- Mapa de calor do ROMI por coorte

## Etapa 6: Conclusões e Recomendações
- Consolidação de métricas por origem
- Diagnóstico de canais rentáveis vs problemáticos
- Recomendações estratégicas de alocação de orçamento


## 💡 Recomendações Estratégicas
1. Redistribuição Imediata do Orçamento (Prioridade Máxima)
- Suspender ou reduzir drasticamente os investimentos na Origem 3 e reavaliar a Origem 4
- Realocar o orçamento para as Origens 1, 2, 5 e 9 (ROI positivo)

2. Estratégias para Aumentar Retenção e LTV
- Implementar programas de email marketing, remarketing e SMS para clientes que compraram no primeiro dia
- Ações de upsell e cross-sell imediatamente após a primeira compra
- Ofertas personalizadas e descontos para segunda compra

3. Otimização por Dispositivo
- Ampliar investimentos em campanhas para Desktop (maior ROI)
- Realizar auditoria de UX/UI no fluxo de compra para dispositivos móveis (Touch)

4. Gestão de Preços e Promoções
- Investigar a tendência de queda no ticket médio
- Evitar promoções agressivas que erodem a rentabilidade


## 📁 Estrutura do Projeto
````
📁 otimizacao_investimentos_marketing_yafisha/
├── 📁 datasets/                    # Dados utilizados
│   ├── visits_log_us.csv           # Log de visitas dos usuários
│   ├── orders_log_us.csv           # Log de pedidos
│   └── costs_us.csv                # Custos de marketing
├── 📁 notebooks/                   # Notebook Jupyter com análise completa
│   └── Projeto_Sprint_8.ipynb
├── 📁 scripts/                     # Scripts Python avulsos
├── README.md                       # Este arquivo
└── requirements.txt                # Dependências do projeto
````

## 📌 Contato
- [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/luizmarques84)
- [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LuizAlmeida)


## 📊 Resumo dos Insights
| Métrica    | Insight    |
|---|---|
| Retenção D1    | 2,6% (oportunidade de melhoria no engajamento)    |
| Conversão D0    | 72,2% (comportamento de compra imediata)    |
| Ticket médio    | R$ 5,00 (baixo, com tendência de queda)    |
| LTV médio    | R$ 6,79    |
| Desktop vs Touch    | Desktop tem ticket 17% maior e LTV 14,9% maior    |
| Investimento total    | R$ 329.131,62    |
| Canais com ROI positivo    | 4 origens (1, 2, 5, 9)    |
| Canais com ROI negativo    | 6 origens (3, 4, 6, 7, 8, 10)    |
| Melhor canal    | Origem 1 (ROI 49,24%, CAC R$ 7,19)    |
| Pior canal    | Origem 3 (ROI -61,43%, CAC R$ 13,49)    |
| Orçamento mal alocado    | 71,4% investido em canais com ROI negativo    |

- Conclusão Estratégica: A Y.Afisha está investindo 71,4% do orçamento em canais que geram prejuízo. A prioridade máxima é redistribuir o orçamento das Origens 3 e 4 para as Origens 1, 2, 5 e 9. Além disso, a empresa deve focar em estratégias de retenção, já que 72,2% das compras ocorrem no primeiro dia e a retenção D1 é de apenas 2,6%.


## ⭐ Este projeto faz parte do meu Bootcamp em Análise de Dados na TripleTen.


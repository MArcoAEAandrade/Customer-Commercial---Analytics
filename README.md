# Customer-Commercial---Analytics
# Performance Comercial — Bank Transactions

## 1. Sobre o projeto

Este projeto apresenta uma análise exploratória de uma base de transações bancárias com mais de 1 milhão de registros, buscando compreender o perfil dos clientes, seus padrões de movimentação financeira e a concentração de valor dentro da carteira.

Mais do que descrever os dados, o objetivo é transformar os indicadores encontrados em **insights comerciais**, identificando diferentes perfis de clientes e possíveis oportunidades de atuação para a instituição financeira.

O projeto foi desenvolvido a partir de um desafio do Kaggle e utiliza **Python, Pandas, SQL, Databricks e visualização de dados**.

---

## 2. Objetivo de negócio

A análise busca responder, inicialmente, quatro perguntas:

* **Quem são os clientes da carteira?**
* **Como o valor financeiro está distribuído entre os clientes?**
* **Como os clientes utilizam o banco?**
* **Onde estão as principais concentrações de clientes e valor?**

A partir desse diagnóstico, a segunda etapa do projeto será direcionada à construção de **segmentações comerciais**, buscando identificar grupos com diferentes níveis de valor, utilização e potencial de relacionamento.

---

# 3. Conhecendo a carteira

Antes de analisar o comportamento financeiro, o primeiro passo foi entender a composição da base.

### Perfil etário

A carteira apresenta idade média próxima de **41 anos**, com maior concentração de clientes na faixa de **36 a 50 anos**.

A segunda faixa mais representativa é a de **26 a 35 anos**, que representa aproximadamente **27% da carteira**.

Esse perfil indica uma base predominantemente adulta, mas com uma participação relevante de clientes mais jovens, o que pode gerar diferentes necessidades e oportunidades de relacionamento.

### Gênero

A distribuição por gênero apresenta uma forte assimetria:

* Masculino: aproximadamente **73%**
* Feminino: aproximadamente **27%**

Ou seja, aproximadamente **3 em cada 4 clientes são homens**.

Esse desequilíbrio deve ser considerado nas análises posteriores, principalmente para evitar que diferenças de comportamento sejam interpretadas sem considerar a composição da própria carteira.

---

# 4. Onde está o valor da carteira?

Depois de compreender quem compõe a base, o próximo passo foi analisar a distribuição do saldo dos clientes.

O primeiro indicador analisado foi o saldo médio.

O resultado apresentou uma diferença significativa entre **média e mediana**:

* **Saldo médio:** aproximadamente R$ 115 mil
* **Mediana:** aproximadamente R$ 16,8 mil

Essa diferença indica uma distribuição extremamente assimétrica.

Enquanto a média é influenciada por clientes com saldos muito elevados, a mediana mostra que o cliente típico possui um saldo significativamente menor.

### O que isso significa?

A média, isoladamente, pode gerar uma percepção distorcida sobre o valor da carteira.

Por isso, foi necessário analisar também a **concentração do saldo entre os clientes**.

---

# 5. Concentração patrimonial

A análise mostrou uma forte concentração de saldo:

> Aproximadamente **10% dos clientes concentram cerca de 76% do saldo total**.

Enquanto isso:

> Os **80% de clientes com menor saldo concentram aproximadamente 12% do saldo total**.

Esse comportamento demonstra que o valor financeiro da carteira não está distribuído de maneira uniforme.

Existe uma pequena parcela de clientes que concentra uma proporção muito elevada dos recursos.

O comportamento se aproxima do princípio de Pareto, porém apresenta uma concentração ainda mais acentuada do que a tradicional relação 80/20.

### Insight de negócio

Esse resultado sugere que a estratégia comercial não deve tratar toda a carteira da mesma maneira.

É necessário equilibrar duas frentes:

**Escala**

Atender e desenvolver a grande massa de clientes, buscando aumentar utilização, relacionamento e valor ao longo do tempo.

**Gestão de clientes de alto valor**

Identificar e preservar os clientes que concentram uma parcela significativa dos recursos da instituição, potencialmente oferecendo estratégias de relacionamento e retenção diferenciadas.

---

# 6. Como os clientes movimentam o banco?

Depois de identificar onde está o valor, a análise avançou para o comportamento transacional.

A distribuição dos valores das transações mostrou uma concentração relevante em operações de menor e médio valor.

| Faixa de transação  | Participação aproximada |
| ------------------- | ----------------------: |
| Até R$ 100          |                     19% |
| R$ 100 – R$ 500     |                     35% |
| R$ 1.000 – R$ 5.000 |                     23% |
| Acima de R$ 5.000   |                      5% |

A maior concentração está na faixa de **R$ 100 a R$ 500**, representando aproximadamente **35% das transações**.

Também existe uma participação relevante de transações entre **R$ 1.000 e R$ 5.000**.

### Insight de negócio

A análise mostra que **saldo acumulado e comportamento transacional são dimensões diferentes**.

Um cliente pode possuir um saldo elevado, mas realizar poucas movimentações.

Da mesma forma, um cliente com saldo menor pode apresentar alta frequência de utilização.

Essa diferença será importante para a próxima etapa do projeto: **segmentar os clientes não apenas pelo valor financeiro, mas também pelo nível de relacionamento e utilização do banco.**

---

# 7. Onde estão os clientes?

A análise geográfica mostrou uma concentração relevante nos grandes centros urbanos da Índia.

As cinco principais localidades representam aproximadamente **39,6% da carteira**.

Entre os principais destaques estão:

| Localidade | Participação aproximada |
| ---------- | ----------------------: |
| Mumbai     |                   9,88% |
| New Delhi  |                   8,10% |
| Bangalore  |                   7,78% |
| Gurgaon    |                   7,04% |
| Delhi      |                   6,77% |

Mumbai lidera a carteira, concentrando aproximadamente **10% dos clientes**.

New Delhi aparece em seguida, com aproximadamente **8%**, enquanto Bangalore, Gurgaon e Delhi também apresentam participações relevantes.

### Insight de negócio

Existe uma concentração geográfica importante da carteira nos grandes centros urbanos.

Entretanto, quantidade de clientes não significa necessariamente concentração de valor.

Por isso, uma próxima análise será investigar:

> **As regiões que concentram mais clientes também concentram mais saldo?**

Essa comparação permitirá diferenciar **concentração de volume de clientes** de **concentração de valor financeiro**.

---

# 8. Diagnóstico inicial

A análise exploratória revelou quatro características importantes da carteira:

### 1. Carteira predominantemente adulta

A idade média está próxima de 41 anos, com concentração relevante entre 36 e 50 anos.

### 2. Forte concentração de saldo

Uma pequena parcela dos clientes concentra a maior parte dos recursos financeiros.

### 3. Comportamento transacional concentrado em operações de menor e médio valor

A maior parte das movimentações ocorre em faixas relativamente baixas, apesar da existência de clientes com saldos elevados.

### 4. Concentração geográfica

Os principais centros urbanos representam uma parcela relevante da carteira.

---

# 9. Próxima etapa: segmentação comercial

O diagnóstico inicial mostra que **olhar apenas para a média da carteira não é suficiente**.

Os clientes apresentam diferenças importantes em:

* Saldo;
* Frequência de utilização;
* Valor médio das transações;
* Localização;
* Perfil demográfico.

Por isso, a próxima etapa será transformar essas diferenças em **segmentos de negócio**.

A primeira hipótese de segmentação será construída a partir da relação entre:

> **Valor financeiro × Frequência de utilização**

A partir desse cruzamento, será possível investigar grupos como:

| Segmento           | Característica                      | Hipótese comercial           |
| ------------------ | ----------------------------------- | ---------------------------- |
| **Strategic**      | Alto saldo + alta utilização        | Retenção e aprofundamento    |
| **Opportunity**    | Alto saldo + baixa utilização       | Aumentar relacionamento      |
| **Growth**         | Baixo/médio saldo + alta utilização | Desenvolver valor            |
| **Low Engagement** | Baixo saldo + baixa utilização      | Ativação ou menor prioridade |

Esses segmentos ainda são **hipóteses analíticas** e serão validados nas próximas etapas do projeto.

Posteriormente, outras variáveis poderão ser incorporadas para avaliar se técnicas de **clusterização** conseguem identificar grupos de comportamento semelhantes de forma estatisticamente consistente.

---

# 10. Pergunta central da próxima etapa

A partir do diagnóstico inicial, a principal pergunta passa a ser:

> **Quais grupos de clientes apresentam maior potencial comercial e quais estratégias poderiam ser utilizadas para aumentar seu relacionamento com o banco?**

Essa pergunta orientará a segunda etapa da análise.

---

# 11. Tecnologias utilizadas

* Python
* Pandas
* SQL
* Databricks
* Matplotlib
* Jupyter Notebook
* Kaggle

---

# 12. Estrutura do projeto

```text
bank-transactions-analysis/
│
├── data/
│   └── bank_transactions.csv
│
├── notebooks/
│   └── analise_performance_comercial.ipynb
│
├── sql/
│   └── queries.sql
│
├── visuals/
│   └── charts/
│
└── README.md
```

---

# 13. Conclusão inicial

O diagnóstico mostra que a carteira possui uma estrutura bastante heterogênea.

Embora a base tenha mais de 1 milhão de registros, o valor financeiro não está distribuído de maneira uniforme. Uma pequena parcela dos clientes concentra grande parte dos recursos, enquanto a maioria apresenta saldos significativamente menores.

Ao mesmo tempo, o comportamento transacional revela que **valor financeiro, frequência de utilização e tamanho das transações são dimensões distintas do relacionamento com o banco**.

Esse cenário cria uma oportunidade para sair de uma visão puramente descritiva e avançar para uma abordagem de **segmentação e estratégia comercial**, buscando entender não apenas quem são os clientes, mas também:

> **quais clientes possuem maior valor, quais apresentam maior potencial de desenvolvimento e onde existem oportunidades de relacionamento.**


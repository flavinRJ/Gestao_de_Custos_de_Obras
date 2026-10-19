# 🏗️ Dashboard de Gestão de Custos de Obras (Power BI & Python)

🎯 **Projeto de portfólio focado em análise financeira de projetos, controle orçamentário e *Data Storytelling* para o setor de construção civil.**

---

## 📋 Sobre o Projeto
Este projeto simula um cenário real de controle corporativo e engenharia de custos, comparando o **Planejado (Orçado)** versus o **Executivo (Realizado)** em múltiplos empreendimentos de construção civil. 

O objetivo principal é fornecer aos gestores e à diretoria uma visibilidade imediata dos desvios financeiros, fluxo de caixa e gargalos por categoria de insumo (como estrutura, alvenaria, instalações e mão de obra), transformando dados brutos em decisões estratégicas.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Python (Pandas, Jupyter Notebook):** Validação estrutural de dados, verificação de integridade referencial, testes de unicidade de chaves e simulação de cruzamentos relacionais.
* **Cursor (IDE AI-Powered):** Desenvolvimento ágil de scripts de tratamento e estruturação prévia dos dados.
* **Power BI:** Modelagem dimensional em *Star Schema*, criação de medidas avançadas em **DAX**, estruturação de hierarquias e design de relatórios em *Dark Mode*.
* **Git & GitHub:** Versionamento e documentação do projeto.

---

## 📊 Arquitetura e Modelagem de Dados
O modelo de dados foi estruturado seguindo o padrão de mercado **Star Schema (Modelo Estrela)**, garantindo alta performance e correta propagação de filtros:

* **Tabelas Dimensão:** `dObras` (dados cadastrais e gestores) e `dMateriais` (categorias, insumos e preços base).
* **Tabelas Fato:** `fOrcamento` (metas e custos planejados) e `fCustosReais` (transações e pagamentos efetuados com carimbo de data).

---

## 📈 Principais Métricas e Medidas (DAX)
O painel conta com medidas dinâmicas criadas para o acompanhamento gerencial:
* **Orçado** = `SUM(fOrcamento[Valor_Total_Orcado])`
* **Realizado** = `SUM(fCustosReais[Valor_Total_Real])`
* **Desvio (R$)** = `[Realizado] - [Orçado]`
* **Desvio (%)** = `DIVIDE([Desvio], [Orçado])`

---

## 🖼️ Doutrina Visual do Dashboard

### Página 1 — Visão Executiva
* **KPIs Globais:** Visão imediata do Orçamento Total (R$ 2,06 Mi), Custo Realizado (R$ 1,38 Mi), Taxa de Execução (67,05%) e Variação Percentual (-32,95%).
* **Matriz Hierárquica:** Permite navegar detalhadamente entre os **Gestores** e as **Obras** sob sua responsabilidade.
* **Gráfico de Rosca:** Distribuição percentual do realizado por **Categoria de Material** (evidenciando que a categoria *Estrutura* concentra cerca de 79,8% dos custos).
* **Comparativo por Obra:** Gráfico de barras lado a lado evidenciando o desempenho financeiro de cada empreendimento (*Edifício Jardins*, *Residencial Horizonte* e *Reforma Comercial Centro*).

### Página 2 — Análise Temporal & Detalhe de Insumos
* **Evolução Temporal:** Gráfico de linhas do fluxo de caixa e desembolsos reais ao longo dos meses.
* **Comparativo de Desvio por Insumo:** Identificação exata de quais materiais ou serviços geraram maiores desvios de orçamento.
* **Tabela Detalhada:** Cruzamento completo de categorias, materiais, valores orçados e realizados linha a linha.

---

## 🚀 Como Executar / Visualizar o Projeto
1. Clone este repositório ou faça o download dos arquivos.
2. O arquivo base com os dados brutos estruturados está em `Gestao_Custos_Obras.xlsx`.
3. O script de validação inicial em Python pode ser consultado no notebook `analise.ipynb`.
4. O arquivo de relatório interativo do Power BI encontra-se disponível na raiz do repositório.

---

## 📬 Contato
* **Autor:** Flávio Brandão (`flavinRJ`)
* **LinkedIn:** [Seu Link do LinkedIn](https://linkedin.com/in/fláviodatascience)
* **GitHub:** [https://github.com/flavinRJ](https://github.com/flavinRJ)

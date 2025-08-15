# Análise Exploratória de Dados - Catálogo de Filmes Netflix

## 📜 Visão Geral do Projeto

Este projeto apresenta uma Análise Exploratória de Dados (EDA) completa de um dataset com mais de 9.000 filmes, simulando um cenário de negócio para a Netflix. O objetivo principal é transformar dados brutos em insights estratégicos, respondendo a questões que poderiam guiar decisões de aquisição e produção de conteúdo na plataforma.

Todo o processo, desde a limpeza dos dados até a geração dos insights finais, foi documentado em um Jupyter Notebook.

---

## 🎯 Questões de Negócio Analisadas

A análise foi guiada para responder às seguintes questões:

1.  Qual o gênero de filme mais frequente no catálogo?
2.  Como os filmes se distribuem entre as diferentes categorias de avaliação criadas?
3.  Qual filme possui a maior pontuação de popularidade?
4.  Quais filmes possuem a menor pontuação de popularidade?
5.  Qual ano registrou o maior número de lançamentos de filmes?

### 🔗 [Clique aqui para acessar o Notebook com a análise completa.](netflix_movie_data_analysis.ipynb)
---

## 🛠️ Pipeline da Análise

O projeto seguiu um pipeline estruturado de análise de dados:

* **1. Coleta e Inspeção dos Dados:** Carregamento do dataset a partir de um arquivo `.csv` e inspeção inicial da estrutura, tipos de dados e valores ausentes/duplicados.

* **2. Limpeza e Pré-processamento:**
    * Conversão da coluna `Release_Date` para o formato `datetime` e posterior extração do ano.
    * Remoção de colunas irrelevantes (`Overview`, `Poster_Url`, etc.) para otimizar a análise.
    * Tratamento da coluna `Genre`, que continha múltiplos valores em uma única string, utilizando as técnicas de **`.split()`** e **`.explode()`** para permitir a análise individual de cada gênero.

* **3. Engenharia de Features:**
    * Criação de uma coluna categórica `Vote_Average` a partir de valores numéricos (técnica de *binning* por quartis), simplificando a análise de performance.
    * Otimização do uso de memória através da conversão de colunas de texto com alta repetição para o tipo `category`.

* **4. Análise Exploratória e Visualização:**
    * Utilização de métodos como `.describe()`, `.value_counts()` e `.groupby()` para extrair estatísticas e responder às questões.
    * Criação de visualizações claras e objetivas com **Matplotlib** e **Seaborn** (histogramas e gráficos de barras) para comunicar os resultados.

---

## 💡 Principais Insights Gerados

* **O Gênero 'Drama' Domina o Catálogo:** `Drama` é o gênero mais frequente, aparecendo em mais de 3.700 filmes, o que sugere ser um pilar na estratégia de conteúdo da plataforma.

* **Sucesso de Blockbusters:** O filme de maior popularidade é **`Spider-Man: No Way Home`**, destacando a importância de grandes franquias e eventos cinematográficos para o engajamento máximo do público.

* **Crescimento Exponencial da Produção:** A produção de filmes cresceu exponencialmente ao longo das décadas, com um pico acentuado no período de **2010-2020**, indicando um catálogo focado em conteúdo recente.

* **Baixa Popularidade Diversificada:** Dois filmes distintos (`The United States vs. Billie Holiday` e `Threads`) empataram como os menos populares, mostrando que o baixo engajamento não é restrito a um único tipo ou era de conteúdo.

---

## 💻 Ferramentas e Bibliotecas Utilizadas

* **Python 3**
* **Pandas:** Para manipulação e análise dos dados.
* **NumPy:** Para operações numéricas.
* **Matplotlib & Seaborn:** Para visualização de dados.
* **Jupyter Notebook:** Como ambiente de desenvolvimento interativo.

---

## 🔗 Contato

*Para mais informações sobre o projeto, me encontre no LinkedIn!*

[Seu Nome no LinkedIn](SEU_LINK_AQUI)
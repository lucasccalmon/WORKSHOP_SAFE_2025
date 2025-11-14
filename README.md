# Predição de Resultados no Futebol Usando a Distribuição de Poisson

Este repositório demonstra a aplicação do modelo de **Distribuição de Poisson** para prever resultados de partidas de futebol. Utilizando dados da Série A do Campeonato Brasileiro, o projeto calcula as capacidades ofensivas e defensivas das equipes para estimar a probabilidade de diferentes placares finais.

## Conteúdo do Notebook

1.  **Importação de Bibliotecas**: Configuração inicial do ambiente com `pandas`, `numpy`, `matplotlib` e `seaborn` para manipulação, análise e visualização de dados.
2.  **Carregamento e Limpeza de Dados**: Os dados dos resultados da Série A do Campeonato Brasileiro são extraídos de `fbref.com` (com tratamento para evitar erros de acesso) e processados para incluir apenas as informações relevantes e corrigir inconsistências.
3.  **Extração de Gols**: Separação dos gols marcados por mandantes e visitantes a partir da coluna de resultados.
4.  **Cálculo de Médias de Gols**: Determinação das médias de gols marcados e sofridos por equipes em casa e fora, servindo como base para as capacidades ofensivas e defensivas.
5.  **Previsão de Gols por Equipe**: Aplicação do modelo de Poisson para prever o número provável de gols que cada equipe marcará em um confronto específico.
6.  **Cálculo de Probabilidades de Placares**: Geração de uma matriz de probabilidades que mostra a chance de cada placar final possível, acompanhada de um heatmap para visualização.
7.  **Análise de Probabilidades**: Cálculo e interpretação das probabilidades de vitória para cada equipe e de empate.

## Metodologia

O modelo se baseia na Distribuição de Poisson, que é adequada para eventos raros que ocorrem a uma taxa média conhecida (neste caso, gols por partida). As capacidades ofensivas e defensivas de cada time são calculadas com base em seus históricos de gols marcados e sofridos, ajustadas pelas médias gerais do campeonato.

## Como Usar

O notebook é estruturado para ser executado sequencialmente. Ele pode ser adaptado para prever resultados de outras partidas, bastando alterar os times e a URL da fonte de dados.

## Melhorias Futuras

Para aprimorar o modelo, poderíamos incorporar:

-   Dados de múltiplas temporadas para maior robustez.
-   Ponderação de resultados mais recentes (suavização exponencial) para refletir mudanças de elenco ou técnico.
-   Inclusão de variáveis adicionais (lesões, suspensões, qualidade do gramado, histórico de confrontos diretos, etc.).

Este projeto oferece uma introdução simples, mas eficaz, ao mundo das predições esportivas baseadas em dados.

https://colab.research.google.com/drive/1Iw_GHxndopZTmJH7Go9VW3kJirZdcUkP?usp=sharing
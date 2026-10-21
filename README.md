# Projeção do 2º turno 2026 — Lula x Flávio

Página pública: https://arthurrochac.github.io/lulaxflavio/

Projeção estatística independente feita a partir de dados públicos (resultados oficiais do TSE e pesquisas registradas). **Não é pesquisa eleitoral.**

## Como está organizado
- `index.html` — a página (modelo, gráficos e explicações). Todas as contas rodam no navegador.
- `data/*.json` — os dados de entrada. As atualizações automáticas mexem só nesta pasta:
  - `pesquisas.json` — pesquisas registradas usadas na média
  - `apuracao.json` — apuração oficial do TSE no domingo (linha `uf: "BR"` = nacional)
  - `atualizacoes.json` — histórico de mudanças mostrado na página
  - `premissas.json`, `transferencias.json`, `base_1t.json`, `oficial_1t.json`, `historico.json`, `erros_historicos.json`, `apuracao_1t.json` — base fixa do modelo
- `d3.min.js` — biblioteca de gráficos (D3 v7.9.0), incluída para a página não depender de serviços externos.

A página relê os arquivos de `data/` a cada 10 minutos (a cada 1 minuto no dia 25/10).

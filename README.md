# Entrega do Projeto Final

## Grupo
- Gregório Xavier Nascimento Pereira 2601820
- Leonardo Hasselmann 2602356
- Lucas Alves de Carvalho 2601908
- Lucas Gomes Fernandes Alonso 2603004 
- Lucas Ramos da Siva 2602996

## Funcionalidade 1 — Novas cidades e sensação térmica

- [x] O pipeline contempla 7 cidades cadastradas em `config.py`.
- [x] Belém e Curitiba foram adicionadas à configuração.
- [x] A variável `apparent_temperature` é buscada na API.
- [x] A coluna `sensacao_c` passa pela limpeza.
- [x] As colunas `sensacao_media` e `sensacao_max` são criadas na visão diária.
- [x] As colunas novas são persistidas no SQLite.
- [x] A API devolve `sensacao_media` e `sensacao_max` em `/clima/diario`.
- [x] O dashboard mostra `sensacao_media` no comparativo e na tabela.
- [x] Os comandos `python -m` de `cleaner`, `aggregator` e `sqlite_repository` rodam sem erro.

## Funcionalidade 2 — Resumo do período

- [x] `python -m clima_pipeline.transform.resumo` calcula os valores esperados com dados mockados.
- [x] O endpoint `/clima/resumo` foi criado.
- [x] O endpoint devolve 404 para cidade inexistente ou período sem dados.
- [x] O `/clima/diario` continua usando o mesmo filtro de período, agora centralizado em `_filtrar_periodo`.
- [x] O dashboard mostra cartões de resumo para cada cidade selecionada.
- [x] Os cartões usam o período escolhido na barra lateral.
- [x] `docs/api/transform.rst` e `README.md` foram atualizados.

## Prints

![Pipeline rodando para 7 cidades](prints/logpipeline.png)
![Endpoint de resumo na API](prints/getlogs.png)
![Dashboard com resumo](prints/dashboard.png)
![Grafico de Temperatura](prints/grafico1.png)
![Grafico Comparativo Cidades & Tabela Agregada](prints/grafico2.png)

## Observação

A parte mais delicada foi garantir que a sensação térmica atravessasse todas as etapas do pipeline. A solução foi seguir o caminho do dado arquivo por arquivo: configuração, limpeza, agregação, persistência, schema, API e dashboard.

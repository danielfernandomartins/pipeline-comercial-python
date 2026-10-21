# Pipeline comercial em Python

Aplicação interativa de estudo para cadastrar oportunidades e calcular indicadores básicos. Complementa o portfólio de dados com prática de Python e regras comerciais.

[Notebook](pipeline_comercial_v1.ipynb) · [Abrir no Colab](https://colab.research.google.com/github/danielfernandomartins/pipeline-comercial-python/blob/main/pipeline_comercial_v1.ipynb)

## Funcionalidades implementadas

- Cadastrar cliente, produto, valor e status.
- Listar oportunidades registradas.
- Somar valores em aberto nos status `prospeccao` e `negociacao`.
- Contar oportunidades ganhas e perdidas.
- Somar o valor das oportunidades ganhas.
- Calcular ganhas / total de oportunidades cadastradas × 100.

O denominador da taxa inclui oportunidades abertas. Portanto, ela difere da taxa de ganho sobre oportunidades encerradas: ganhas / (ganhas + perdidas).

## Exemplo de conferência

Com uma oportunidade ganha de R$ 100, uma perdida de R$ 50 e uma em negociação de R$ 200:

| Indicador | Resultado esperado pelas regras |
|---|---:|
| Total de oportunidades | 3 |
| Valor em aberto | R$ 200 |
| Valor ganho | R$ 100 |
| Ganhas / total cadastrado | 33,33% |
| Ganhas / encerradas, para comparação conceitual | 50% |

A última métrica não é calculada pela versão atual.

## Como executar

Abra o notebook no Jupyter ou Colab e execute a célula do programa. Use o menu de 1 a 5; escolha 5 para encerrar. A aplicação usa apenas recursos nativos do Python.

## Limitações verificadas no código

- Dados apenas em memória; reiniciar a execução limpa os registros.
- Não há edição de status ou histórico de transições.
- Não há validação de status, valores negativos ou campos vazios.
- Entradas não numéricas no valor podem interromper a execução.
- Sem filtros temporais, persistência, dashboard ou testes automatizados.

## Próximas melhorias

Validar entradas e explicitar as duas definições de conversão; depois adicionar persistência e análises por período. São evoluções planejadas, não funcionalidades concluídas.

**Autor:** Daniel Fernando Martins. Projeto de estudo, sem alegação de resultados empresariais.

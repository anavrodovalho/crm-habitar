# CRM Habitar

Quadro Kanban dos leads da Habitar Imoveis. A pagina le os dados, em tempo real, da planilha
`Habitar_Leads` atraves de um app da web do Google Apps Script, e grava de volta apenas a coluna **Status**.

**Acesse:** https://anavrodovalho.github.io/crm-habitar/

## Como conectar

Ao abrir pela primeira vez, a pagina pede dois dados:

1. **Link do app da web** do Apps Script (termina em `/exec`);
2. **Senha (TOKEN)** definida dentro desse mesmo script.

Os dois ficam guardados no navegador de quem abriu (`localStorage`) - nada e enviado para este repositorio
nem fica escrito no codigo. Sem esses dados a pagina nao mostra lead nenhum.

Quem ja esta conectado pode gerar, pela engrenagem, um link pronto para enviar a outra pessoa.

## O que fica salvo no navegador

| Chave | Conteudo |
|---|---|
| `crm_habitar_config` | link do app da web + senha |
| `crm_habitar_cache` | ultima resposta da planilha (abre instantaneo) |
| `crm_habitar_notas` | notas pessoais por lead |
| `crm_habitar_filtros` | filtros ativos |

O **Status nao fica no navegador**: a fonte da verdade e sempre a planilha.

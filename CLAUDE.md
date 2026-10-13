# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Estado do projeto

O repositório ainda não tem código. Não há comandos de build, lint ou testes por enquanto.

## Cofre de acessos (Site no Ar)

As credenciais do projeto ficam no web-app **aulas-cofre** do Site no Ar, não neste repositório:

- URL: https://aulas-cofre.sitenoar.app
- Site id: `01a135c6-6982-7379-bb48-ac1b6b471770` (use o id, não o slug, nas ferramentas do Site no Ar)
- Secrets: `ADMIN_PASSWORD` (login do painel), `REPLICATE_API_TOKEN`, `ANTHROPIC_API_KEY`,
  `WP_URL`, `WP_USER`, `WP_APP_PASSWORD` (senha de aplicativo do WordPress).
- Os secrets só são cadastrados pelo link de `request_secret_input` (expira em ~15 min). Nunca peça
  valores no chat nem os escreva em arquivos. Depois de cadastrar, faça um novo `deploy` para o
  Worker passar a ler os valores.
- O código do app vive no repositório do próprio Site (editado pelas ferramentas `mcp__Site_no_Ar__*`);
  o `AGENTS.md` de lá descreve a estrutura.

## Sessões do grupo "aulas 1p"

As sessões do projeto são agrupadas pela tag `aulas-1p`:

- **Coordenador** (`aulas-1p:coordenador`): conversa com o usuário e delega tarefas.
- **Funcionários** (`aulas-1p:funcionario`): executam as tarefas delegadas, cada um no seu branch, e
  reportam ao coordenador com `send_message`. Não abrem PRs nem mexem no Site no Ar ou em secrets
  sem pedido explícito.
  - Funcionário 1: `session_01AAY81yX8CZL3BtxuTFuK9Y`, branch `claude/aulas-1p-funcionario`.
  - Funcionário 2: `session_01RcbJy1Y8R7owirYv5bJFyy`, branch `claude/aulas-1p-funcionario-2`.

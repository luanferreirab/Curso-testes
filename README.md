# Curso de Testes

Projeto em TypeScript para praticar testes automatizados com Jest em um dominio simples de compras.

O codigo trabalha com duas entidades principais:

- `Produto`: valida nome, preco, estoque, desconto e controla descricao e movimentacao de estoque.
- `Pedido`: adiciona e remove produtos, calcula total, finaliza compras e gera um resumo do pedido.

## Objetivo

Este repositorio foi montado como base de estudo para:

- exercitar TDD e escrita de testes unitarios;
- validar regras de negocio pequenas, mas reais;
- usar builders para facilitar a montagem de cenarios de teste;
- evoluir uma suite de testes de forma incremental.

## Tecnologias

- TypeScript
- Jest
- ts-jest
- ts-node
- terminal-kit

## Estrutura

```text
  compras/
    src/
      Produto.ts
      Pedido.ts
      index.ts
    testes/
      Produto.test.ts
      Pedido.test.ts
      utils/
        ProdutoBuilder.ts
    jest.config.js
    package.json
    README.md
```

## O que ja esta coberto

No estado atual do projeto:

- `Produto` possui uma bateria de testes ja implementada.
- A suite cobre criacao, validacoes, descontos, ajuste de estoque e descricao.
- `Pedido` ja possui a estrutura dos cenarios com `test.todo`, servindo como roadmap para proximos testes.

Isso torna o projeto bom para estudar tanto testes concluidos quanto expansao de cobertura.

## Como executar

Entre na pasta do projeto Node:

```bash
cd compras
```

Instale as dependencias, se necessario:

```bash
npm install
```

Rode os testes:

```bash
npm test
```

Gere relatorio de cobertura:

```bash
npm run test:coverage
```

Execute a aplicacao no terminal:

```bash
npm start
```

## Como o projeto ensina testes

Alguns pontos interessantes deste codigo:

- `ProdutoBuilder` reduz repeticao nos testes e deixa o setup mais legivel.
- As validacoes de construtor mostram bem o uso de `toThrow`.
- O comportamento de desconto permite testar cenarios percentuais e fixos.
- Os `test.todo` em `Pedido` ajudam a planejar os proximos casos antes da implementacao.

## Proximos passos sugeridos

Se a ideia for evoluir o projeto, o caminho natural e:

1. implementar os testes de `Pedido`;
2. endurecer as regras de finalizacao e validacao do pedido;
3. corrigir textos com problemas de codificacao;
4. adicionar testes de integracao simples entre `Produto` e `Pedido`.

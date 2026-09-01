# Fechamento Mensal · Milhas Plus

PWA instalável (PC e celular) para registrar lançamentos por conta, companhia e fonte, e gerar o relatório de fechamento no layout da arte original.

## Arquivos

```
index.html   app inteiro (interface, cálculos e relatório)
manifest.json
sw.js        cache offline
icons/       icon-192.png, icon-512.png, icon-maskable-512.png
```

## Publicar no GitHub Pages

1. Crie o repositório e envie os arquivos mantendo a estrutura de pastas.
2. Em **Settings → Pages**, escolha a branch `main` e a pasta `/ (root)`.
3. Abra o endereço gerado. Precisa ser HTTPS para o service worker funcionar.

## Instalar

- **Android/Chrome:** menu ⋮ → Adicionar à tela inicial. O botão “Instalar app” também aparece no topo.
- **iPhone/Safari:** Compartilhar → Adicionar à Tela de Início.
- **PC:** ícone de instalar na barra de endereço.

## Como funciona

- **Cadastros:** responsáveis, contas (clientes) com responsável e cor próprios, companhias e fontes das milhas.
- **Lançamentos:** data, conta, companhia, fonte e valor. O campo “repetir” cria vários lançamentos iguais de uma vez.
- **Painel:** escolha o mês e o responsável. Em “Mais filtros” você refina por conta, companhia, fonte e faixa de valor (de/até). Os filtros aplicados aparecem no topo do relatório, então o PDF já sai identificado.
- **Consolidado por responsável:** bloco próprio no relatório, com total, percentual e as contas de cada um. Só aparece quando há responsável cadastrado.
- **Ajustes:** título, nome que aparece ao lado do título, quantas linhas mostrar antes de agrupar em “Outros”, backup e restauração.

## Exportar

- **Salvar em PDF** usa a impressão do navegador (escolha “Salvar como PDF”).
- **Baixar imagem** gera um PNG. Precisa de internet na primeira vez, porque carrega a biblioteca html2canvas.
- **Resumo p/ WhatsApp** abre o WhatsApp com o texto do fechamento pronto.

## Dados

Ficam no `localStorage` do aparelho. Cada dispositivo tem sua própria base. Use **Ajustes → Baixar backup** antes de trocar de celular ou limpar o navegador.

A aba **Lançamentos** tem os mesmos filtros, mais o filtro por conta, e mostra a soma do que está filtrado.

O app começa com os dados de exemplo de Agosto/2026 (os mesmos da arte). Apague-os em **Ajustes → Apagar tudo** ou remova as contas em Cadastros quando for usar de verdade.

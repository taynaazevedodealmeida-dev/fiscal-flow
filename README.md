# Fiscal Flow

Ferramenta web de página única que organiza e categoriza automaticamente suas Notas Fiscais eletrônicas (NF-e / NFC-e em XML). Feita para o MEI e a pequena empresa brasileira que vive afogado em nota fiscal.

**Tudo roda 100% no seu navegador.** Nenhum arquivo é enviado para servidor algum — sem cadastro, sem chave de API, sem instalação.

## O que faz

- Arraste ou selecione um ou vários XMLs de NF-e/NFC-e.
- Extrai número, data de emissão, fornecedor (nome + CNPJ), valor total e itens de cada nota.
- Categoriza cada despesa automaticamente por palavra-chave (combustível, alimentação, software, material de escritório, frete, serviços, telecom, outros).
- Mostra tabela consolidada, resumo por categoria, total geral e gráfico de barras.
- Exporta um CSV pronto para entregar ao contador (abre direto no Excel pt-BR).

## Como abrir

Dê **duplo clique** no arquivo `index.html`. Ele abre no seu navegador padrão. Não precisa de internet depois de aberto — funciona offline.

## Como usar

1. Clique em **Selecionar arquivos** (ou arraste os XMLs para a área pontilhada).
2. Sem arquivo em mãos? Clique em **Carregar nota de exemplo** para ver a ferramenta funcionando.
3. Confira a tabela e o gráfico por categoria.
4. Clique em **Exportar CSV para o contador** para baixar o consolidado.

## Editando as regras de categoria

O motor de categorização fica no `<script>` do `index.html`, na constante `REGRAS`. Cada linha é `{ nome, palavras:[...] }`. Para criar uma categoria nova, adicione uma linha. Acentos e maiúsculas são ignorados na comparação.

## Privacidade como argumento de venda

Como nada sai do navegador, dados fiscais sensíveis nunca trafegam pela internet nem ficam em nuvem de terceiros. Isso é uma vantagem real de venda frente a SaaS tradicionais que exigem upload das notas.

## Como ganha dinheiro (sem investimento inicial)

- **Freemium:** grátis até 20 notas/mês. Acima disso, plano pago (ex.: R$ 19/mês) libera notas ilimitadas, histórico salvo e relatórios.
- **Fechamento mensal assistido:** serviço pago em que consolidamos e revisamos as notas do mês e entregamos o relatório pronto para o contador.
- **Sem custo de infra:** por ser 100% client-side, hospedar é praticamente de graça (GitHub Pages / Netlify free). Margem alta desde a primeira venda.

## Tecnologia

HTML + CSS + JavaScript puro, em um único arquivo. Leitura de XML via `DOMParser`. Exportação via `Blob`. Sem dependências externas, sem build.

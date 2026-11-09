# AgingCross

Ferramenta web de página única para cruzar planilhas: preenche e confere a coluna **MAS** de uma planilha de AGING a partir de uma base de referência indexada por **BSAO / House ID**. Tudo roda no navegador, nenhum arquivo é enviado para servidor.

Online: https://sousax.github.io/AgingCross/index..html

## Funcionalidades

- Upload por clique ou arrastar e soltar de um ou mais arquivos `.xlsx`, `.xls` ou `.csv` para a base de referência e para a base a conferir.
- Detecção automática da linha de cabeçalho (primeira linha, entre as 16 iniciais, com pelo menos 4 células preenchidas) e sugestão das colunas pelo nome (ex.: "Ref. DSV", "Contra File", "Ref. Minebea", "Text", "Reference Key 3").
- Coluna de ID principal e alternativa em cada base: se a principal não tiver ID válido, usa a alternativa.
- Normalização do ID: reconhece `BSAO0283110`, House IDs como `IAH0360253` e Shipment IDs com `S` inicial (`SIAH0360253` vira `IAH0360253`).
- Classificação de cada linha: preenchido automaticamente, já preenchido (OK), divergente (MAS existente diferente do encontrado), sem correspondência na referência ou ID não localizado.
- Resumo com totais e prévia das primeiras 50 linhas.
- Download da planilha original atualizada (`Atualizado_<nome>.xlsx`), alterando só as células de MAS preenchidas.

Só a primeira aba de cada arquivo é lida.

## Tecnologias

- HTML, CSS e JavaScript puro, num único arquivo
- [SheetJS (xlsx) 0.18.5](https://sheetjs.com/) via CDN

## Como rodar

Abra `index..html` no navegador (precisa de internet para carregar o SheetJS do CDN).

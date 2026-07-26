# console — a face do console de pedidos

`index.html` é **autocontido**: sem build, sem framework, sem CDN. Uma página só,
que fala com a API do GitHub pelo `fetch`.

## Destino

Este arquivo é para viver num repositório **público** próprio (`superjurista-console`),
servido pelo GitHub Pages — Pages em repositório privado exige conta paga, e a página é
casca vazia: nenhum dado mora nela.

Está aqui só até esse repositório existir. A fila de pedidos continua nas issues de um
repositório **privado**, informado em Ajustes.

## Ver sem GitHub

    python3 -m http.server 8931 --bind 127.0.0.1
    # abrir http://127.0.0.1:8931/index.html?demo=1

O `?demo=1` mostra a fila com pedidos de mentira, em todos os estados. Nada é enviado.

## O dígito verificador

A conferência do número CNJ (módulo 97, ISO 7064) é a mesma de `scripts/lib/pedido.py`.
A paridade entre as duas foi verificada em 6.000 números (3.000 válidos e 3.000 com o
dígito errado de propósito): zero divergências.

Aqui ela é **conveniência** — erro de digitação custa zero segundo em vez de quarenta
minutos. Quem decide de verdade é o guarda, no Mac.

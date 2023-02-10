# Ferramenta de busca baseada em texto
Uma text-based search engine (em nível de prova de conceito) com os objetivos de: 

Dado uma plataforma de busca de produtos 

1) ajudar o usuario a encontrar os produtos desejados;  
2) ajudar o usuario a descobrir novos itens que o surpreenda

# Sobre o modelo
Adotei um modelo baseado em "bag of words" (BM25) para representar o score de relevancia. O modelo busca por produtos que contem ao menos uma palavra da query e faz uma filtro por popularidade (mostrando apenas pos rodutos com um numero minimo de vendas) e um filtro de relevancia com a query (apenas produtos com um score minimo sao mostrados ao cliente).

O algoritmo calcula o score de relevancia com a query BM25 da categoria, tags e título individualmente. O score final de relevancia por produto por query é uma combinação linear dos scores individuais de categoria, titulo e tags, na forma:

![Alt text](equation_image.png?raw=true "modelo linear")

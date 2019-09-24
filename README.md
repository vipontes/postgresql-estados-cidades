# postgresql-estados-cidades

## Descrição
Este script cria uma estrutura no PosgreSQL contendo as regiões, estados e cidades do Brasil.

No momento contempla 5570 cidades.

## Instalação

Crie um banco de dados vazio no pgAdmin ou qualquer outra ferramenta e execute o script

## Query de teste

``` sql
-- Exemplo de pesquisa
SELECT c.cidade_id, c.cidade_nome, e.estado_nome, e.estado_sigla, r.regiao_descricao
FROM cidade c
INNER JOIN estado e ON c.estado_id = e.estado_id
INNER JOIN regiao r ON e.regiao_id = r.regiao_id
ORDER BY regiao_descricao, estado_nome, cidade_nome;
```
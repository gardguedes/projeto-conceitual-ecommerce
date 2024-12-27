# Desafio: Refinando a Modelagem do Cenário E-commerce

## Descrição do Desafio
Refinar a modelagem do cenário de e-commerce.

## Narrativa
Objetivo: vender produtos
Entidades: produto, estoque, cliente, pedido, fornecedor 

### Entidade: Produto
- Terceiros podem vender na loja
- Cada produto possui um fornecedor
- Um ou mais produtos podem compor um pedido

### Entidade: Cliente
- O cliente pode ser PF ou PJ
- O endereço do cliente determinará o valor do frete
- Um cliente pode comprar mais de um pedido
- há um período de carência para devolução

### Entidade: Pedido
- Cliente cria um pedido
- Um ou mais produtos podem compor um pedido
- O pedido pode ser cancelado
- Antes de enviar um pedido, ele pode ser cancelado.

### Entidade: Fornecedor
- É possível ter vários fornecedores
- Cada fornecedor pode ter vários produtos

### Entidade: Estoque
- Está em local determinado

## Objetivos do Desafio
Refine o modelo apresentado acrescentando os seguintes pontos:
- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
- Entrega – Possui status e código de rastreio;

## Decisões de Modelagem
- Para realizar a inclusão das informações de CPF e CNPJ optei por criar as entidades PF e PJ, para separar essas informações e depois relacionar com a entidade CLIENTE.
- Já para o pagamento, criei a entidade PAGAMENTO e PAGAMENTO POR CARTÃO, para especificar esse tipo de pagamento, pois possui várias informações e dessa forma é possível identificar o cartão por ID e nome. Sendo possível ter mais de um cartão cadastrado no pagamento.
- Decide tornar a ENTREGA uma entidade, pois tem informações que são importantes e precisam ser armazenadas, como staus e código de rastreio. Além dessa entidade, crie EMPRESA DE ENTREGA, para ter as informações das empresas responsáveis pela entrega.

## Resolução do Desafio

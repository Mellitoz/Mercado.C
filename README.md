# Mercado em C - README
# Descrição do Projeto
Este projeto é um sistema simples de gerenciamento de mercado desenvolvido em linguagem C. O sistema permite o cadastro de produtos, listagem de produtos, adição de produtos ao carrinho, visualização e remoção de itens do carrinho, e finalização do pedido com cálculo do valor total da compra. O objetivo é demonstrar o uso de estruturas de dados (structs), arrays e funções em um programa modular.

# Funcionalidades do Sistema
# 1. Cadastro de Produto

•	O usuário pode cadastrar novos produtos com um código único, nome e preço.

•	Antes do cadastro, o sistema exibe a lista de produtos já cadastrados. Caso não existam produtos, é exibida uma mensagem "Nenhum produto cadastrado, cadastre um Agora.".

# 2. Listar Produtos

•	Exibe todos os produtos cadastrados no sistema, mostrando o código, nome e preço (com o símbolo $).

•	Permite ao usuário verificar os produtos disponíveis para compra.

# 3. Compra de Produtos

•	Lista os produtos disponíveis para que o usuário saiba quais produtos estão disponíveis para compra.

•	Permite ao usuário selecionar um produto pelo seu código e adicionar uma quantidade específica ao seu carrinho.

•	Se o produto já estiver no carrinho, a quantidade será atualizada ao em vez de duplicar o produto.

# 4. Visualizar Carrinho

•	Exibe todos os produtos que estão no carrinho, mostrando o código, nome, quantidade, preço do item e subtotal.

# 5. Remover Produto do Carrinho

•	Lista os produtos do carrinho para facilitar a escolha do usuário.

•	O usuário pode especificar o código do produto a ser removido e a quantidade que deseja remover.

•	A quantidade que será removida não poderá exceder a quantidade disponível no carrinho.

•	Se a quantidade do produto no carrinho se tornar zero, o produto é removido do carrinho.

# 6. Fechar Pedido

•	Calcula o valor total da compra e exibe uma fatura detalhada com os produtos, suas quantidades e subtotais.

•	Limpa o carrinho após a finalização do pedido.

# 7. Sair

•	Encerra o programa com uma mensagem de agradecimento.

# Estrutura de Dados

•	Produto: Estrutura que armazena os dados do produto:

o	int codigo: Código exclusivo de cada produto.

o	char nome[50]: Nome do produto.

o	float preco: Preço do produto.

•	Carrinho: Estrutura que armazena os produtos adicionados ao carrinho e a quantidade de cada um:

o	Produto produto: Produto selecionado.

o	int quantidade: Quantidade do produto no carrinho.

# Como o Sistema Foi Desenvolvido
O sistema foi desenvolvido em C, utilizando estruturas (structs) para representar os produtos e os itens no carrinho. Arrays estáticos são usados para armazenar até 50 produtos e até 50 itens no carrinho.

Funções foram criadas para modularizar as operações principais do sistema:

•	Mello(): Gerencia o fluxo do programa e as opções do usuário.

•	cadastro(): Permite o cadastro de novos produtos, listando os produtos cadastrados previamente.

•	lista(): Exibe todos os produtos cadastrados.

•	comprar(): Lista os produtos disponíveis e permite ao usuário adicionar produtos ao carrinho.

•	verCarrinho(): Exibe os produtos que estão no carrinho.

•	remocao(): Permite a remoção de produtos do carrinho, verificando se a quantidade desejada é existente

•	pagar(): Calcula e exibe o valor total da compra e limpa o carrinho.

•	prodsCarrinho(): Verifica se um produto está no carrinho.

•	pegarProdCod(): Retorna um produto baseado no código informado.

•	infos(): Exibe as informações de um produto, incluindo o preço em reais

# Como Compilar e Executar

# Pré-requisitos

•	Compilador GCC instalado
.
•	Um terminal ou prompt de comando.

# Passo a Passo para Compilar

1.	Salve o código em um arquivo chamado mercado.c.
   
2.	Abra o terminal e navegue até o diretório onde o arquivo mercado.c está salvo.
   
3.	Use o seguinte comando para compilar o programa:
   
gcc mercado.c -o mercado

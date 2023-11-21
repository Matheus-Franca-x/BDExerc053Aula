# BDExerc053Aula

## Exercício 9:

### Estoque:
Código(PK)	|Nome(ÚNICO)	|Quantidade	|Valor(Valor > 0)	|Cód. Editora(FK)	|Cód. Autor(FK)
-|-|-|-|-|-
10001	|Sistemas Operacionais Modernos 	|4	|108.00	|1	|101
10002	|A Arte da Política	|2	|55.00	|2	|102
10003	|Calculo A	|12	|79.00	|3	|103
10004	|Fundamentos de Física I	|26	|68.00	|4	|104
10005	|Geometria Analítica	|1	|95.00	|3	|105
10006	|Gramática Reflexiva	|10	|49.00	|5	|106
10007	|Fundamentos de Física III	|1	|78.00	|4	|104
10008	|Calculo B	|3	|95.00	|3	|103

### Editora:
Código(PK)	|Nome	|site
-|-|-
1	|Pearson	|www.pearson.com.br
2	|Civilização Brasileira	
3	|Makron Books	|www.mbooks.com.br
4	|LTC	|www.ltceditora.com.br
5	|Atual	|www.atualeditora.com.br
6	|Moderna	|www.moderna.com.br

### Autor:
Código(PK)	|Nome	|Breve Biografia
-|-|-
101	|Andrew Tannenbaun	|Desenvolvedor do Minix
102	|Fernando Henrique Cardoso	|Ex-Presidente do Brasil
103	|Diva Marília Flemming	|Professora adjunta da UFSC
104	|David Halliday	|Ph.D. da University of Pittsburgh
105	|Alfredo Steinbruch	|Professor de Matemática da UFRS e da PUCRS
106	|Willian Roberto Cereja	|Doutorado em Lingüística Aplicada e Estudos da Linguagem
107	|William Stallings	|Doutorado em Ciências da Computacão pelo MIT
108	|Carlos Morimoto	|Criador do Kurumin Linux

### Compra:
Código(PK)|	Cod. Livro(PK)(FK)	|Qtd Comprada(Qtd > 0)	|Valor(Valor > 0)	|Data Compra(PK)
-|-|-|-|-
15051	|10003	|2	|158.00	|2020-07-04
15051	|10008	|1	|95.00	|2020-07-04
15051	|10004	|1	|68.00	|2020-07-04
15051	|10007	|1	|78.00	|2020-07-04
15052	|10006	|1	|49.00	|2020-07-05
15052	|10002	|3	|165.00	|2020-07-05
15053	|10001	|1	|108.00	|2020-07-05
15054	|10003	|1	|79.00	|2020-08-06
15054	|10008	|1	|95.00	|2020-08-06

## Consultar:
- Nome, valor unitário, nome da editora e nome do autor dos livros do estoque que foram vendidos. Não podem haver repetições.
- Nome do livro, quantidade comprada e valor de compra da compra 15051
- Nome do livro e site da editora dos livros da Makron books (Caso o site tenha mais de 10 dígitos, remover o www.).
- Nome do livro e Breve Biografia do David Halliday
- Código de compra e quantidade comprada do livro Sistemas Operacionais Modernos
- Quais livros não foram vendidos
- Quais livros foram vendidos e não estão cadastrados
- Nome e site da editora que não tem Livros no estoque (Caso o site tenha mais de 10 dígitos, remover o www.)
- Nome e biografia do autor que não tem Livros no estoque (Caso a biografia inicie com Doutorado, substituir por Ph.D.)
- O nome do Autor, e o maior valor de Livro no estoque. Ordenar por valor descendente
- O código da compra, o total de livros comprados e a soma dos valores gastos. Ordenar por Código da Compra ascendente.
- O nome da editora e a média de preços dos livros em estoque.Ordenar pela Média de Valores ascendente.
- O nome do Livro, a quantidade em estoque o nome da editora, o site da editora (Caso o site tenha mais de 10 dígitos, remover o www.), criar uma coluna status onde:
  - Caso tenha menos de 5 livros em estoque, escrever Produto em Ponto de Pedido
  - Caso tenha entre 5 e 10 livros em estoque, escrever Produto Acabando
  - Caso tenha mais de 10 livros em estoque, escrever Estoque Suficiente
  - A Ordenação deve ser por Quantidade ascendente
- Para montar um relatório, é necessário montar uma consulta com a seguinte saída: Código do Livro, Nome do Livro, Nome do Autor, Info Editora (Nome da Editora + Site) de todos os livros
  - Só pode concatenar sites que não são nulos
- Codigo da compra, quantos dias da compra até hoje e quantos meses da compra até hoje
- O código da compra e a soma dos valores gastos das compras que somam mais de 200.00
# Lab06 - Artigo de Dataset Público

Estrutura de pastas:

~~~
├── README.md  <- arquivo apresentando a tarefa
~~~

# Aluno
* `201867`: `Lucas de Paula Soares`

# Análise do Artigo ` PolRoute-DS: um Dataset de Dados Criminais para Geração de Rotas de Patrulhamento Policial `

| campo | valor |
|------------|----------------------------------------|
| referência | `CUNHA SÁ, Bruno; MULLER, Gustavo; BANNI, Maicon; SANTOS, Wagner; LAGE, Marcos; ROSSETI, Isabel; FROTA, Yuri; OLIVEIRA, Daniel. (2021). PolRoute-DS: um Dataset de Dados Criminais para Geração de Rotas de Patrulhamento Policial ` |
| link       | [Link Artigo em PDF](https://drive.google.com/file/d/10Q_T1TANC5BtEBpPexsTv7-gfOLva5X2/view)|
| dataset | [Link PolRoute-DS](https://osf.io/mxrgu/) |
| formato | CSV |

## Resumo

O artigo tem como objetivo disponibilizar um dataset que pode ser utilizado para definição de rotas de patrulhas policiais. Os dados foram extraídos de órgãos externos como por exemplo SSP-SP (Secretaria de Segurança Pública do Estado de São Paulo), nos quais foi possível atribuir um local, data, hora e tipo de ocorrência. Essa ideia está relacionada ao conceito de Cidades Inteligentes (i.e Smart Cities), que vem ganhando muita relevância atualmente. O primeiro passo para construir esse dataset foi extrair os dados relevantes proveniente dos órgãos de segurança pública, em seguida construir um modelo em grafo para a cidade, tomando o cuidado de não deixar uma aresta sendo uma rua toda e sim uma aresta ser um pedaço de uma rua de tamanho fixo e finalmente, linkar tais arestas às ocorrências criminais. Assim, é possível obter um “mapa” de crimes para cada região, zona ou cidade. Os dados de criminalidade estão disponíveis, juntamente com o mapa, em https://osf.io/mxrgu/. No instante da publicação do artigo, há dados da cidade de São Paulo.

## Perguntas de pesquisa/análises

Em vista do artigo, e com os dados publicado, poderíamos fazer as seguintes perguntas/análises:
* Qual a rua com maior índice de roubos de celulares de uma determinada região?
* Qual o principal tipo de ocorrência criminal que há em determinada região?
* Qual o tempo médio entre dois roubos de celulares em uma determinada rua? (Isso poderia indicar a frequência com que há roubos em uma determinada rua, por exemplo: a cada 5 dias, 7 dias, por exemplo)
* Existe alguma relação entre índice de ocorrências criminais e iluminação pública em um determinado segmento? (nesse caso seria preciso integrar com algum banco de dados de iluminação pública da região em questão, e selecionar casos em que a ocorrência foi no período da noite)


## Trabalhos relacionados

Alguns trabalhos mencionados no artigo são:
* Yoo, J. S. (2019). Crime data warehousing and crime pattern discovery. In Proceedings of the Second International Conference on Data Science, E-Learning and Information Systems, DATA ’19, New York, NY, USA. Association for Computing Machinery
* Spadon, G., Scabora, L. C., Oliveira, P. H., Araujo, M. V. S., Machado, B. B., de Sousa, E. P. M., Jr., C. T., and Jr., J. F. R. (2017). Behavioral characterization of criminality spread in cities. In Koumoutsakos, P., Lees, M., Krzhizhanovskaya, V. V., Dongarra, J. J., and Sloot, P. M. A., editors, International Conference on Computational Science, ICCS 2017, 12-14 June 2017, Zurich, Switzerland, volume 108 of Procedia Computer Science, pages 2537–2541. Elsevier. 
  
Tais trabalhos são baseados em um conceito que serviu de inspiração para o artigo, o conceito de Data Warehouse. A diferença é que tais trabalhos tinham interesse em identificar regiões com maior índice de criminalidade, enquanto que o objetivo do artigo em questão é criar uma rota de patrulha policial, por isso a diferenciação nas arestas para saber se é uma via de mão única ou uma via de mão dupla.

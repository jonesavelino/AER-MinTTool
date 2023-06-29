# AER-MinTTool
AER-MinTTool é um protótipo de software que tem como objetivo implementar a abordagem AER-MinT.

# Descrição do Projeto
AER-MinTTool é um protótipo de software que tem como objetivo implementar a abordagem AER-MinT. A abordagem tem como objetivo apoiar o processo de Extração de Relações a partir da busca de pares de rótulos dentro de um Corpus de Textos (conjunto de sentenças), avaliando cada sentença e submetendo-a ao modelo pré-treinado, baseado no domínio do problema, utilizando o BERT a fim de produzir uma lista de sugestões para auxiliar o reconhecimento de entidades nomeadas.

# Fonte da Base de dados Textuais para Treinamento
- Neste projeto, foi utilizado como fonte de dados para treinamento o corpus NLM-Chem. O NLM-Chem é um recurso de texto completo anotado manualmente sobre produtos químicos na literatura biomédica com base na publicação de artigos científicos da PubMed associado ao NCBI (National Center for Biotechnology Information). Para a execução dos experimentos foram utilizados parte do corpus, em função da volumetria dos dados, contendo mais de 2 milhões de sentenças. 
- O código-fonte para recuperação dos dados do corpus estão disponíveis no caderno do projeto. 
- Fonte de dados: https://ftp.ncbi.nlm.nih.gov/pub/lu/NLMChem/

# Pré-requisito
Este projeto possui as seguintes dependências:

- [Python 3.9.12] (https://www.python.org/downloads/release/python-3912/) linguagem de programação para rodar as bibliotecas e desenvolvimento.
- [Anaconda Navigator 2.1.4] (https://www.anaconda.com/products/distribution) é uma interface gráfica de usuário (GUI) de desktop incluída na distribuição Anaconda® que permite iniciar aplicativos e gerenciar facilmente pacotes, ambientes e canais conda sem usar comandos de linha de comando.
- [Jupyter Notebook 6.4.11] (https://jupyter.org/install) é um ambiente que oferece essa abordagem de Notebooks cujo objetivo é rodar códigos escritos em Python.
- [GraphDB 9.11] (https://www.ontotext.com/products/graphdb/graphdb-free/) é um banco de dados para lidar com Grafos que permite a manipulação de dados baseados em Grafos RDF e utiliza a linguagem SPARQL para recuperação e processamento de consultas. Além disso, é uma ferramenta que possibilita a descoberta de conhecimento a partir de inferências das relações dos recursos.

- Bibliotecas: 
- [TensorFlow 2.82] é uma biblioteca de aprendizado de máquina.  
- [Seaborn 0.11.2] é uma biblioteca de visualização de dados estatísticos. 
- [Scikit-Learn 1.1.1] é uma biblioteca de aprendizado de máquina e mineração de dados.
- [Scipy 1.8.1] é uma biblioteca científica para Python.
- [Pip 21.2.4] é uma biblioteca recomendada para instalação de pacotes Python.
- [Regex 2022.6.2] é uma biblioteca para lidar com expressões regulares.
- [Pandas 1.4.2] é uma biblioteca de software criada para a linguagem Python para manipulação e análise de dados.
- [NLTK 3.7] é uma biblioteca para lidar com liguagem natural em Python.
- [NumPy 1.22.4] é uma biblioteca para a linguagem de programação Python, que suporta o processamento de grandes, multi-dimensionais arranjos e matrizes, juntamente com uma grande coleção de funções matemáticas de alto nível para operar sobre estas matrizes.
- [Matplotlib 3.5.2] é uma biblioteca de software para criação de gráficos e visualizações de dados em geral, feita para e da linguagem de programação Python e sua extensão de matemática NumPy.
- [Bert-for-tf2 0.14.9] é uma biblioteca que contém a implementação do TensorFlow 2.0 Keras de google-research/bert com suporte para carregamento dos pesos pré-treinados originais e produzindo ativações numericamente idênticas ao calculado pelo modelo original (https://github.com/kpe/bert-for-tf2).

# Experimento
- Para executar o experimento é importante seguir o passo a passo das ações do caderno do projeto.
- 1) Submeter a base de treinamento com os dados da PubMed;
- 2) Rodar as operações de: 
- 2.1) Etapa 1: Importação das bibliotecas;
- 2.2) Etapa 2: Pré-processamento (pré-processamento, instanciação do modelo BERT, tokenização, constituindo as bases de treinamento e de testes);
- 2.3) Etapa 3: Contrução do modelo;
- 2.4) Etapa 4: Treinamento (definição dos hiperparâmetros, execução do treianamento);
- 2.5) Etapa 5: Avaliação
- 2.6) Etapa 6: Submissão de Sentenças (implmentação das def obter_predicao(sentence), busca_final() e gerar_saida()) 
- 2.6.1) Arquivo de entrada com as sentenças a serem avaliadas: avalia.txt
- 2.6.2) Arquivo de saída com a extração das relações encontradas pelo modelo: saida.txt
- 2.6.3) Arquivo de saída do item 2.6.2 (parte) já triplificado (sujeito, predicado e objeto) para ser importado no repositório no GraphDB: saida.n3

# Trabalhos e publicações
- AVELINO, Jones O.; CORDEIRO, Kelli F.; C. CAVALCANTI, Maria. AER-MinT - Apoio ao processo de Extração de Relações baseado em Mineração de dados Textuais. In: SIMPÓSIO BRASILEIRO DE BANCO DE DADOS (SBBD), 37. , 2022, Búzios. Anais [...]. Porto Alegre: Sociedade Brasileira de Computação, 2022 . p. 409-414. ISSN 2763-8979. DOI: https://doi.org/10.5753/sbbd.2022.226201.
- Acesso ao artigo: https://sol.sbc.org.br/index.php/sbbd/article/view/21828

# Ecossistema e Profissões em Big Data

## Plataformas e Soluções de Dados: Data Lake - Uma nova abordagem para o DW

Ralph Kimball – um dos precursores dos conceitos de Data Warehouse e da técnica de modelagem dimensional – menciona na terceira edição do famoso best-seller “The Data Warehouse Toolkit”:

!["Ralph Kimball"](/images/05_EcossistemaProfissoesEmBigData/kimball.png)<br/> - Ralph Kimball - Fonte: Banco de imagens Shutterstock(2016).

* Estes termos recorrentes (se referindo a grande parte dos conceitos de DW/BI) já existem há mais de três décadas.

* Recolhemos toneladas de dados, mas não podemos acessá-los, precisamos “slice e dice” os dados em todas as direções (quebrar um conjunto de informações em partes menores permitindo examiná-lo a partir de diferentes pontos de vista para que possamos compreendê-lo melhor).

* Pessoas de negócios precisam obter os dados facilmente.

* Mostrar apenas o que é importante.

* Desperdiçamos reuniões inteiras discutindo sobre quem tem os números corretos ao invés de tomar decisões.

* Queremos usar a informação para apoiar a tomada de decisão baseada em fatos.

Os primeiros estudos sobre a abordagem Data Warehouse surgiram na década de 1980 como conceitos acadêmicos. Naturalmente, a sistematização das empresas com ERP, CRM e os demais sistemas transacionais ajudaram a criar as fontes de dados corporativas que alavancaram a necessidade da implementação de uma base de dados também conhecida como armazém de dados (o DW), com o objetivo de consolidar uma visão estratégica dos dados, organizados na linha do tempo de acordo com as necessidades de negócio.

Consequentemente, os dados evoluíram, as fontes de dados da era digital são bastante expansivas e possuem uma variedade de dados muito maior.

Não proponho discutirmos a importância e a necessidade de trabalharmos com DW, pois isso é evidente. Big Data não anula o Data Warehouse que foi projetado para atender soluções de Business Intelligence, o mercado não terá uma resposta rápida e definitiva para qualquer tipo de comparações neste sentido. Mas realmente precisamos considerar o apoio das plataformas de Big Data para compor uma arquitetura de Data Warehouse tradicional, portanto, podemos afirmar que os domínios são complementares.

A arquitetura do Data Warehouse não está preparada para atender ao Big Data, por várias razões:

* Toda e qualquer nova fonte de dados deverá passar por um processo burocrático de estruturação (modelagem, ETL, ajustes etc.) e quanto maior o volume e abrangência dos dados, maior será o tempo necessário para armazenamento e processamento.

* As tecnologias de armazenamento e processamento tradicionais não atendem as capacidades das demandas de negócio. E os 3Vs de Big Data excedem seus limites facilmente.

* O custo de soluções tradicionais de DW, considerando licenciamento de software, armazenamento, processamento e segurança, dificultam e até inviabilizam os projetos de evoluções.

James Dixon (2015), Diretor de Tecnologia na Pentaho mencionou em seu blog “Union of the State – A Data Lake Use Case” que para facilitar o pensamento sobre Data Mart, basta pensar como uma reserva de água engarrafadas, higienizadas, embaladas e estruturada para fácil consumo, fazendo uma analogia com o objetivo de preparar os dados para o fácil consumo.

!["Data Marts"](/images/05_EcossistemaProfissoesEmBigData/dataMarts.png)<br/> - Data Marts - Fonte: Banco de imagens Shutterstock(2016).

Os Data Marts são parte de um domínio de dados, orientados aos departamentos ou assuntos da empresa por exemplo.

Bill Inmon é considerado o pai do Data Warehouse e assim como Kimball possui dezenas de livros sobre o assunto. Um ponto de divergência curioso e conhecido, entre os dois, está relacionado aos Data Marts.

!["Bill Inmon"](/images/05_EcossistemaProfissoesEmBigData/billInmon.png)<br/> - Bill Inmon - Fonte: Banco de imagens Shutterstock(2017).

Kimball & Ross (2013) defende iniciar a construção dos Data Marts e integrá-los posteriormente, definindo o conceito que apelidou de Data Warehouse Bus Architecture.

Na avaliação de Inmon (1995) é recomendável criar um Data Warehouse com um único modelo de dados corporativo e posteriormente derivar, construindo os Data Marts por assuntos ou departamentos, propondo o conceito do CIF – Corporate Information Factory.

!["Kimball vs Inmon"](/images/05_EcossistemaProfissoesEmBigData/kimballXinmon.png)<br/> - Kimball vs Inmon - Fonte: FIAP(2017).

Independentemente da opção sobre as melhores práticas de implementação dos Data Marts, James Dixon propôs em Dixon (2017) o termo Data Lake para contrastar a abordagem dos Data Marts. De acordo com o autor, existem duas grandes limitações na abordagem de Data Marts:

* Apenas um subconjunto dos atributos é analisado, para que apenas perguntas predeterminadas possam ser respondidas.

* Os dados são agregados e perdemos visibilidade para os níveis mais baixos.

Estes problemas são muitas vezes definidos como silos de informações e acabam criando dificuldades para a evolução de modelos analíticos.

A EMC está criando um “Data Lake” em conjunto com a White House Climate Data Initiative, com o objetivo de compreender os dados climáticos e suas implicações quanto ao aquecimento da Terra entre outros possíveis fatores. Para este “Data Lake” a premissa é que quanto maior o número de pessoas adicionando mais dados, maior será o impacto.

Foi realizado um estudo inicial com a seguinte questão: para onde foram 1 milhão de Andorinhas e qual é o motivo?

!["Para onde foram as andorinhas?"](/images/05_EcossistemaProfissoesEmBigData/andorinhas.png)<br/> - Para onde foram as andorinhas? - Fonte: Banco de imagens Shutterstock (2017).

Para entender como as mudanças climáticas afetam até mesmo uma ave durante o ano, comece multiplicando os milhões de aves por milhares de locais, todos os dias, durante 365 dias.

Essa visualização de big data revelou tudo isso em apenas alguns segundos e pode fazer mais, muito mais. Os cientistas conseguem ver rapidamente as mudanças na migração, observando os dados de vários anos. A migração está aumentando? E a temperatura? E as chuvas? Há correlações que apontam para as mudanças climáticas?

Data Lake é um repositório de armazenamento e engine para processamento de Big Data. Fornece armazenamento massivo para qualquer tipo de dados, tem enorme poder de processamento e capacidade de lidar com tarefas e jobs simultâneos, praticamente ilimitadas.

Um conceito chamado Data Lake e não uma tecnologia, isso significa que pode ir além da solução Hadoop. Porém o Ecossistema Hadoop é a tecnologia que melhor atende as necessidades definidas pelo conceito do Data Lake, seu custo- benefício acaba sendo decisivo para que as empresas iniciem uma prova de valor (PoV) e evoluam com a implementação.

!["Data Lake"](/images/05_EcossistemaProfissoesEmBigData/dataLake.png)<br/> - Data Lake - Fonte: FIAP (2017).

Esta arquitetura possibilita manter um grande repositório de dados “brutos”, preservando o princípio de imutabilidade, garantindo maior capacidade de retenção de dados com custo consideravelmente reduzido.

Um modelo tradicional de ETL (Extract/Transform/Load) ou Extração/ Transformação/Carga, exige um esforço grande para modelagem e desenvolvimento de rotinas para preparar os dados. Aplicando a abordagem de Data Lake, o processo de carga poderá ser priorizado, com a possibilidade de abrir mão da estruturação dos dados inicialmente, assim podemos iniciar o processo de ingestão (carga) de dados no Data Lake e já submetermos os dados aos processos de análises.

Todavia, nem todos os dados devem ser tratados de forma bruta, ainda continuaremos dependendo de processos pesados de transformação dos dados para grande parte dos dados, envolvendo técnicas de estruturação, enriquecimento e qualidade dos dados. Fazendo uso da grande capacidade do cluster de armazenamento, podemos otimizar o processo com um fluxo invertido, conhecido como ELT.

Aplicando o ELT, é possível usar a capacidade do cluster Hadoop para executar processamentos massivos, aumentando a velocidade e agilidade de todo o processo.

Mantendo o princípio de imutabilidade (não alterando os dados no Data Lake) será possível corrigir erros de regras de negócios e falhas de cadeias de transformação sem a necessidade de grandes manobras e esforços adicionais para movimentações de dados.

O Data Lake armazena um grande volume de dados independentemente do seu formato ou estrutura, e não define um esquema, mantendo o dado no seu formato nativo até que os dados sejam efetivamente demandados.

O modelo propõe despejar todos os dados no lago, seguindo a abordagem “free-for-all”. Com o tempo, não será tão simples navegar por grandes lagos escuros com pouca visibilidade, passando por brejos improdutivos que limitaria o potencial dos dados.

!["Analogia a navegar por grandes lagos escuros"](/images/05_EcossistemaProfissoesEmBigData/lagosEscuros.png)<br/> - Analogia a navegar por grandes lagos escuros - Fonte: Banco de imagens Shutterstock (2017).

Precisamos considerar técnicas importantes como a curadoria, para manter as águas claras e passíveis de navegação, afinal nosso maior objetivo é extrair o valor dos dados com agilidade.

    A Curadoria dos dados envolve a captura de metadados e gestão da linhagem dos dados, incorporando as informações no catálogo de metadados. Está intimamente ligado à governança dos dados e será importante para sustentar os processos de análise, estruturação, limpeza e transformação dos dados.

Com toda a confusão e volume de informações que estamos produzindo, é cada vez mais necessária a adoção da curadoria como premissa para um projeto de Big Data, fator decisivo para a sustentação do Data Lake.

Um exemplo de curadoria usado em redes sociais é o Moments do Twitter
(https://twitter.com/i/moments).

!["Exemplo de curadoria Moments do Twitter"](/images/05_EcossistemaProfissoesEmBigData/momentsTwiter.png)<br/> - Exemplo de curadoria Moments do Twitter - Fonte: Twitter (2017).

Com um grande volume e tweets gerados a cada segundo versus vários assuntos, não é simples construirmos um roteiro sobre os fatos e qualificarmos os conteúdos com base em colaborações. Afinal, não temos possibilidade de seguir todas as pessoas e acompanhar um grande número de publicações a todo o momento.

!["Usuário twittando"](/images/05_EcossistemaProfissoesEmBigData/usuarioTwittando.png)<br/> - Usuário twittando - Fonte: Banco de imagens Shutterstock (2017).

O Twitter aposta em parcerias com empresas especializadas em conteúdo para fazer o trabalho de curadoria e apresentar aos usuários os moments (ou histórias) que serão complementadas com os tweets de usuários que representem relevância para os assuntos discutidos.

O Twitter aposta em parcerias com empresas especializadas em conteúdo para fazer o trabalho de curadoria e apresentar aos usuários os moments (ou histórias) que serão complementadas com os tweets de usuários que representem relevância para os assuntos discutidos.

---

## Plataformas e Soluções de Dados: Arquitetura LAMBDA

Processamento de grandes volumes e análises com baixíssima latência (real time), são grandes desafios inclusive para a arquitetura de Big Data.

Nathan Marz propôs o termo Arquitetura Lambda (LA) para o design genérico de processamento de dados escalável e tolerante a falhas, após experiências com processamentos distribuídos na Backtype e Twitter.

A arquitetura Lambda atende as características de Big Data e Fast Data, sendo uma base de referência para implementação dos mais variados use cases.
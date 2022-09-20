# Tratamento de dados obtidos através do TOPAS utilizando Python

## Geant4

o Geant4 é uma plataforma desenvolvida em C++ utilizada para simular a passagem de partículas pela matéria usando o método de Monte Carlo. Você pode encontrar mais informações sobre o Geant4 [aqui](https://geant4.web.cern.ch/).

## TopasMC

O topasMC utiliza como base o Geant4 com o intuito de tornar simulações MonteCarlo, como na área de Física Médica, mais simples. Ele dispõe de diversas ferramentas muito úteis para o desenvolvimento de simulações na radioterapia, por exemplo.

A licença do TOPAS pode ser obtida após o preenchimento do formulário disponível em [Registration for License](http://www.topasmc.org/registration). Nele é necessário preencher um formulário onde é possível selecionar a opção gratuita para aqueles que querem utilizar o software para fins didáticos ou de pesquisa. Com o preenchimento do formulário você será convidado a assistir a palestra e dessa forma receber a licença. O TOPAS tem como pré-requisito ser instalado em uma máquina com sistema operacional macOS ou utiliza o Kernel Linux. Caso você utilize Windows temos dois caminhos para solucionar esse problema: fazer um dual boot em seu computador ou utilizar uma máquina virtual. Com o sistema operacional adequado você deve baixar o pacote de código TOPAS, disponível em code repository, apropriado para seu sistema operacional. No caso do Linux, esse arquivo está separado em duas partes. Após, é possível fazer toda a instalação do TOPAS através do terminal, ferramenta disponível que recebe instruções do usuário. Inicialmente é necessário instalar alguns pacotes que possuem, por exemplo, bibliotecas fundamentais para o funcionamento do TOPAS, como libexpat1. Logo após seguimos para o download dos arquivos referentes ao TOPAS. Todo o processo de instalação está disponível na página [TOPAS Installation Guide](http://www.topasmc.org/user-guides/installation).

De acordo com o site oficial do TopasMC, o custo da licença por usuário varia de Gratuito a US$ 2.500, dependendo da classe de usuário. [Aqui](http://www.topasmc.org/) você pode encontrar mais informações sobre o TopasMC e as formas de obter a licença. 

## Tratamento de dados

O tipo de arquivo que vamos utilizar como *output* é o `.csv` (Comma-separated values) que separa valores por vírgula. Veja como esse arquivo é apresentado para o usuário: 

![image](https://user-images.githubusercontent.com/66263337/171259331-f437d7d2-54b7-48aa-b087-42642136c225.png)

Esse arquivo nos fornece informações sobre a versão utilizada do TOPAS, nesse caso 3.7, o arquivo `.txt` utilizado, o número de bins em X, Y e Z e a dose correspondente. 

Nosso objetivo é encontrar o gráfico como o disponível abaixo, onde conseguimos observar a Porcentagem de Dose em Profundidade (PDP). 

![image](https://user-images.githubusercontent.com/66263337/171262799-7e2e9cdf-eed6-49d2-b5b9-e588afe0c6f2.png)


Com o `.csv` obtido podemos iniciar o tratamento de dados. Ele pode ser feito manualmente com ferramentas como *excel* ou *LibreOffice* e outras, como QtiPlot para o desenvolvimento dos gráficos.
Esse repositório contém a automatização desse processo utilizando a linguagem de programação Python e suas bibliotecas. As versões utilizadas estão disponíveis abaixo: 

* Python      3.9.7
* pandas      1.3.4
* matplotlib  3.4.3

Estamos disponibilizando dois tipos de arquivo. O arquivo `.py` é um arquivo de programa (ou script) escrito em python, podendo ser executado através do terminal, da seguinte forma:

`python nomedoarquivo.py`

e com isso seguir as instruções pedidas. 

Temos também o arquivo `.ipynb`. Esse é um documento de notebook usado pelo Jupyter notebook. O Jupyter notebook é um aliado dos desenvolvedores e cientistas de dados que facilita o trabalho com dados tanto em Python como em outras linguagens, como o R. 

Recomendamos o uso desse arquivo, visto que ele está descrevendo o que cada um dos comandos está fazendo. Caso precise, escolha utilizá-lo deixo abaixo um tutorial de como baixar e executar na sua máquina. 

* **Para Windows**

É recomendado fazer o Download do Anaconda disponível [aqui](https://www.anaconda.com/products/distribution). O Anaconda visa simplificar o uso e gerenciamento de alguns pacuts de linguagens, como python e R. 
Assim que instalação estiver concluída você verá um novo terminal disponível com o nome `Anaconda Prompt`. Execute esse programa e vá até o diretório que deseja criar o arquivo usando o comando `cd`. Por exemplo:

`cd OneDrive/Documentos`

Nesse diretório execute `jupyter notebook`. 

![image](https://user-images.githubusercontent.com/66263337/171267134-a471f9b9-aba7-4ca9-b449-6abd77cf2b35.png)

No seu navegador você verá uma tela como essa:

![image](https://user-images.githubusercontent.com/66263337/171267057-e1034f28-79b7-4bc3-a6fc-aeb2e28f5686.png)

Observação: é provável que seja necessário instalar as bibliotecas `pandas` e `matplotlib` utilizando `conda install pandas matplotlib`.

* **Para Linux**

A primeira coisa que devemos fazer é atualizar os pacotes com `sudo apt-get update`. 

Depois disso instalamos o gerenciador do pacotes do python pip e o python (caso não tenha) com o comando `sudo apt-get -y install python python-pip python-dev`.

Instalamos as duas bibliotecas necessárias, com o comando `pip install pandas matplotlib`.

Por fim, instalamos o jupyter notebook com o comando `sudo apt-get -y install ipython ipython-notebook`. 

### **Tanto usuários de Linux, quanto de Windows devem ficar atentos a uma coisa:**

Em um momento do código é necessário fornecer o nome do arquivo output que deve ser analisado. 

![image](https://user-images.githubusercontent.com/66263337/171267535-2f5c83ae-cc50-4d6a-8499-32749a49fc3a.png)

É importante notar que o arquivo deve estar na mesmo pasta que o arquivo `.ipynb`, como o `eletrons16MeVCampo10x10.csv`. Caso contrário encontraremos um erro.

## Exemplo de execução

Fornecendo os parâmetros desejados:

![output](https://user-images.githubusercontent.com/66263337/174501369-6a4d5505-12e6-41c9-9968-d4bb4a0375e5.gif)

Executando linha a linha:

![output2](https://user-images.githubusercontent.com/66263337/174501734-19983150-2622-4198-a7f1-05fcc31ebbd8.gif)


## Referências

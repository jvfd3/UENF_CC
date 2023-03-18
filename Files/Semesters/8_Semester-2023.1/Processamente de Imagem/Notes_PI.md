# Processamento de imagem

## Aula 1 - 07/03/23 - 1/4 - Não teve por poucos alunos

## Aula 2 - 09/03/23 - 2/4

### Processamento de imagens

Computação Gráfica VS Computação visual

Grandes áreas da computação gráfica: Análise de imagens X Síntese de Imagens X Processamento de imagens

Síntese: Criar imagens
Análise:
Processamento:

<!-- GIF de clustering -->
<!-- GIF de neurônios processando quais números foram manuscritos -->

### Imagem digital

- A imagem é representada em uma região discreta.
- Conjuntos de tuplas RGB definem os pontos
- Pode ser Uni, bi ou tri dimensional -> Um único pixel, uma imagem, um voxel
- Binária, monocromática, multibanda ou colorida -> Preto e branco; Escalas de cinza; RGB
- Vetorial ou matricial (SVG vs Raster)

### Off-topic

Leandro foi pro IMPA e agora tá em Coimbra
Rivera queria ir para a Inglaterra ou Canadá, mas deixaram ele na fila de espera. No Brasil logo aceitaram ele na PUC. Ele também passou pro sul, mas teria que esperar dois meses para começar a receber bolsa, então ele foi pra PUC.
Drones que percorrem a selva para analisar bichinhos através de padrões.
Câmeras em sala de aula para identificar o comportamento dos alunos
Análise de imagens é que nem uma aeromoça passar na frente de uma turbina de avião. Entra uma coisa e sai outra coisa.
Geraldo faleceu há pouco tempo. Era um bom matemático
Em 2015 fizeram um projeto financiado para analisar as assinaturas por diversos métodos diferentes
Na época em que ele fazia faculdade não havia tira teima de jogo de futebol. O Globo financiou. Se mapeia o jogo e coloca sobre um mapa pré desenhado. Isso em 1998. Não sabe se atualmente continua sendo do trabalho que ele fez só que aprimorado ou se é algo novo.
Todo mundo está abrindo a porta, o que será que está acontecendo? Procurando algum ladrãozinho?

### Relação entre áreas

Mineração em banco de dados X visão computacional X IA

<!-- Imagem grandona -->

### Sistemas de imagens digitais

#### Processamento de imagens - PI

- Manipulação de imagens
- Refere-se aos dados de entrada, e também os de saída
- Rearranjo dos pontos/pixels da imagem
- Exemplo: Redução de ruído, realce de imagem, restauração de imagens, etc.

Para detectar ruído, precisa-se de alguma heurística para determinar os padrões.

#### Análise de imagens - AI

- Interpretação de informações da imagem através de algoritmos computacionais
- Tomam imagens como entradas, mas produzem outros tipos de saída
- Obter parâmetros descritivos da imagem
- Usada para realização de reconhecimento de padrões, visão computacional ou de extração de conhecimento das imagens (Mineração de imagens)

#### Síntese de imagens - SI

- Criação de imagens por computador
- Transforma dados em imagens, que podem ser consideradas na forma vetorial ou matricial como as iamgens médicas de ressonância magnética, ultrassom e tomografias.
- Pode usar técnicas de AI que inserem objetos reais e modelos de textura nos objetos e cenas geradas

#### Visão computacional - VC

- Extração de informações de imagens (AI) e identificação e classificação de objetos nesta imagem.
- Aplicações: reconhecimento de pessoas , de assinaturas e de objetos; inspeção de peças em linhas de monstagem; orientação de movimentos de robôs em indústrias automatizadas; etc.
- Utiliza AI e IA (ou técnicas de tomada de decisão).

## Aula 3 - 14/03/23 - 2/4 - [..., 15h36]

### Visão computacional (slide)

#### Etapas de um Sistema de Visão computacional (Pattern Recognition)

Análise qualitativa:
    Aquisição/Digitalização
    -(pixels)->
    Restauração/Realce
    -(Pixels)->
    Segmentação
    ->
    Grupos de Pixels
Análise quantitativa:
    Grupos de Pixels
    Extração de atributos/características ->
    -(Dados)->
    Classificação/Reconhecimento
    -(Grupos de dados)->
    Decisão

Diferença entre quantização e segmentação: (ele explicou mas eu tava tentando fazer o diagrama)

A diferença é:

Segmentação: separar regiões da imagem que apresentem características em comum para dar uma amenizada na quantidade de informações de alguma forma.
Quantização: Redução da gama de cores disponíveis para apenas um determinado valor em um intervalo de 0 a 255.

#### Aquisição de imagens

A aquisição de imagens se dá através da conversão da cena real (3D) em uma imagem (2D), sendo essa a função da câmera.

- Imagem
  - Energia luminosa distribuída numa posição espacial, podendo ela ser dada por $R+T+A=1$, onde:
    - $A$: Absorvida
    - $T$: Transmitida
    - $R$: Refletida
  - Pontos (x, y) da imagem com itensidade é dado por $intensidade(x, y) = I(x, y) * R(x, y)$, onde:
    - $I$: Iluminação
    - $R$: Refletância
  - Pontos que definem a imagem:
    - Discreto: amostragem ou quantização
    - Resolução: maior ou menor

#### Amostragem e quantização

- Amostragem
  - Pelo que entendi, diferente da amostragem da estatística que pega um conjunto de dados aleatoriamente, nesse caso ele meio que cria parcelas de pixels próximos e cria meio que uma média delas.
  - Dá para fazer isso em situações de maior curvatura (observando a derivada), e criando segmentos mais largos quando a variabilidade for baixa e segmentos mais finos quando a variedade é grande.
- Quantização
  - Definição da quantidade de níveis de tons atribuídos a cada ponto
- Imagens reais apresentam númeors ilimitados de cores e tons
- Imagens computacionais
  - Limitado nível de cores ou tons
  - Um pixel seria uma amostra de uma quantização

#### Resolução

Quanto maior a resolução, maior o número de pixels. Geralmente associado à uma boa qualidade de imagem, entretanto, também significando um maior número de informações.

#### Quantização

A variação da gradação tonal afeta a qualidade da imagem.
Haver grande resolução e gradação tonal permite imagem nítida.

A quantização acontece da seguinte forma:
primeiro pega todos os 256 níveis de cinza
depois conta quantos pixels de cada nível existem
pega os 16 com maior quantidade e então esses englobam os outros pontos.

#### Realce e restauração

- Operações básicas em processamento de imagens
  - Realce
    - Destacar detalhes da imagem como contorno
  - Restauração
    - Destaque de segmentos deteriorados
    - Compensa deficiências na aquisição
    - Busca modelo formal (matemático) para restaurar

Paramos aqui

## Aula 4 - 16/03/23 - 1/4 - [14h30?, ...]

### OffTopic

Fernando Linhares é sobrinho de Pedro Linhares, que era da primeira turma
Outro que também era da primeira turma é o Élisson

### Visão computacional (slide) (2)

#### Segmentação

- Isolar regiões de pontos da imagem pertencentes a objetos para posterior extração de atributos e cálculos de parâmetros descritivos

Operação: limiarização ou separação por tom do corte.
limiarização: conseguir definir os limites
Exemplo: objeto e fundo, através da limiarização binária (thresholding) 0 e 1

##### Processo de segmentação

Algoritmo:

Para cada pixel, se a escala de cinza de um pixel é menor que o limiar, converte para preto, senão, pra preto.

Como determinar valor de limiar? "Várias formas"

Uma delas seria fazer um histograma das escalas de cinza, traçar um gráfico e selecionar algum dos vales que trace uma boa divisão entre a quantidade de brancos e pretos

Vetor de histograma (VU) é usado para definir o limiar.

Pode-se usar o vetor de histograma para usar o método de tsu (ou tzu).

Análise de profundidade: vai varrendo características em comum para tentar alcançar algum tipo específico de resultado.

#### Extração de atributos ou Características

A partir de imagens já segmentadas ou binárias, busca obter dados relevantes ou atributos das regiões ou objetos destacados.
Exemplos:

- Número de objetos
- Dimensões - Medidas X e Y
- Geometria
- Propriedades de luminosidade e textura
  - Cores
  - Nível de intensidade médio
    - Distribuição tonal
    - Histograma dos canais da imagem
  - Desvio padrão de cada banda da região
  - Outros momentos estatísticos: formas de definir onde estão as concentrações de dados

Uma forma de analisar assinaturas seria fazer um histograma de quantos pretos e brancos, (ou quantas trocas de preto pra branco e de branco pra preto) existem em cada uma das colunas e linhas.

Outra forma seria calcular o centro de massa

##### Momentos invariantes

Se fizermos espelho, translação, escala e rotação, o momento estatístico se mantém.

Calcula-se através de Momentos de Hu. Que são momentos estatísticos. Resultando em 7 valores diferentes

Um aluno da primeira turma usou isto para fazer uma rede neural de entendimento dos gestos de mão para interagir com um jogo.

Geometria projetiva: considerando um espaço máximo e mínimo de movimentação da mão, dá para definir o espaço por onde o cursor pode passar como uma interpolação da escala da mão

Usando a normalização ele conseguiu lidar bem com os valores

FIM DA AULA

## Aula 5 - 21/03/23 - x/4 - [..., ...]

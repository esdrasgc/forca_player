# forca_player
## Agente para jogo da forca, a partir da contagem de probabilidade 

### Sobre o projeto
O presente projeto objetiva a criação de um agente para jogo da forca, a partir da contagem de frequência de letras no conjunto de palavras possíveis. A ideia (explicitada em mais detalhes no arquivo demo.ipynb), é escolher sempre a letra mais frequente e realizar a filtragem do conjunto de palavras possíveis a cada nova tentativa. Esse algoritmo baseia-se na estratégia de que, a letra mais frequente tem boa chance de aparecer em mais palavras, bem como, uma filtragem eficiente sobre as palavras, visando uma maior quantidade de subconjuntos de respostas possíveis (se uma letra aparece em mais palavras, porém sempre em posições parecidas, a filtragem sobre os casos totais é inferior a uma bem distribuída nas palavras).   

Com isso, foi possível criar algo semelhante a uma árvore de decisão, dividindo sempre o conjunto de palavras em pelo menos dois grupos (o grupo sem a palavra e o grupo com a palavra numa dada posição). Por outro lado, como as letras tendem a estar distribuídas nas palavras, em especial para o caso da letra mais frequente (escolhida sempre pelo algoritmo), o conjunto de palavras que contêm a letra tentada subdivide-se em vários, permitindo que, ao acertar uma letra, uma fração do conjunto anterior se mantenha. Permitindo ao agente acertar a palavra, após tentar todas as letras presentes na palavra. Como pode ser visualizado no arquivo demo.ipynb, essa estratégia alcança uma acurácia superior a 95%.   


### Resultados
Abaixo é possível visualizar o resultado de uma simulação com 1000 jogos, apresentando as vidas restantes ao fim do jogo, em que o agente venceu em 97% deles:  

<img src="simulacao_1000 jogos.png">



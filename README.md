#  Jogo da velha com algoritmos de inteligência artificial

Este é um programa que permite jogar o jogo da velha contra três jogadores artificiais que utilizam diferentes algoritmos de inteligência artificial para fazer as jogadas:

 - JogadorRandom: escolhe uma jogada aleatória
 - JogadorMinimax: utiliza o algoritmo Minimax para escolher a melhor jogada
 - JogadorMaxmin: utiliza o algoritmo Maxmin para escolher a melhor jogada
 
O programa foi implementado em Python e consiste em duas classes principais:

-   Jogador: representa um jogador genérico e define a interface que deve ser implementada pelos jogadores artificiais
-   JogoDaVelha: controla a lógica do jogo e interage com os jogadores

O arquivo `jogo_da_velha.py` contém o código completo do programa. O jogo pode ser iniciado executando o arquivo.
## Código
O código é uma implementação do jogo da velha com três jogadores artificiais. Cada jogador é representado por uma classe, e todos herdam da classe base `Jogador`, que define os métodos básicos que cada jogador deve ter.

Os jogadores artificiais são:

-   `JogadorMaxmin`: esse jogador usa o algoritmo `maxmin` para escolher a melhor jogada. O `maxmin` é um algoritmo de busca em árvore que avalia todos os possíveis movimentos de cada jogador e escolhe o que leva ao melhor resultado possível para o jogador atual. A cada nível da árvore, o algoritmo alterna entre maximizar e minimizar a pontuação, por isso o nome `maxmin`. Esse jogador é uma versão mais sofisticada do `JogadorMinimax`.
    
-   `JogadorMinimax`: esse jogador usa o algoritmo `minimax` para escolher a melhor jogada. O `minimax` é um algoritmo de busca em árvore que avalia todos os possíveis movimentos de cada jogador e escolhe o que leva ao melhor resultado possível para o jogador atual. A cada nível da árvore, o algoritmo alterna entre maximizar e minimizar a pontuação. Esse jogador é uma versão simplificada do `JogadorMaxmin`.
    
-   `JogadorRandom`: esse jogador escolhe uma jogada aleatória entre as possíveis jogadas no tabuleiro.
    

O método `verifica_resultado` da classe base verifica se o jogo terminou, e em caso afirmativo, qual é o resultado (vitória, derrota ou empate). Ele verifica todas as linhas, colunas e diagonais do tabuleiro e retorna `1` se o jogador `X` venceu, `-1` se o jogador `O` venceu e `0` se o jogo terminou em empate. Se o jogo não terminou, ele retorna `None`.

O método `escolher_jogada` de cada jogador é responsável por escolher qual será a próxima jogada no tabuleiro. Ele recebe o tabuleiro atual como argumento e deve retornar o índice da posição onde o jogador deseja jogar.

O código também define uma função `print_tabuleiro` que imprime o tabuleiro na tela.

## Requisitos

-   Python 3.x

## Executando o programa

Para executar o programa, abra um terminal na pasta onde se encontra o arquivo `jogo_da_velha.py` e execute o comando:

   
    
    python jogo_da_velha.py 
    
    

## Licença

Este programa é um software livre; você pode redistribuí-lo e/ou modificá-lo sob os termos da Licença Pública Geral GNU como publicada pela Fundação do Software Livre (FSF); na versão 2 da Licença, ou (a seu critério) qualquer versão posterior.

Este programa é distribuído na esperança de que possa ser útil, mas SEM NENHUMA GARANTIA; sem uma garantia implícita de ADEQUAÇÃO a qualquer MERCADO ou APLICAÇÃO EM PARTICULAR. Veja a Licença Pública Geral GNU para mais detalhes.



# Jogo de Clique Rápido

Este é um simples jogo de clique rápido criado em JavaScript, HTML e CSS. O objetivo do jogo é clicar no quadrado inimigo que aparece aleatoriamente antes que o tempo acabe. Abaixo, você encontrará uma descrição das partes principais do código.

## Estado do Jogo

O estado do jogo é mantido em um objeto chamado `state`. Ele é dividido em três seções:

### Visão (`view`)

- `squares`: Uma lista de todos os quadrados do jogo.
- `enemy`: O quadrado inimigo que o jogador deve clicar.
- `timeLeft`: Elemento que exibe o tempo restante.
- `score`: Elemento que exibe a pontuação atual do jogador.

### Valores (`values`)

- `gameSpeed`: A velocidade em milissegundos com a qual o inimigo aparece aleatoriamente.
- `hitPosition`: A posição do quadrado inimigo que o jogador deve clicar.
- `result`: A pontuação atual do jogador.
- `currentTime`: O tempo restante no jogo.

### Ações (`actions`)

- `timerId`: Um identificador para o intervalo que controla a geração aleatória do quadrado inimigo.
- `countDownTimerId`: Um identificador para o intervalo que controla a contagem regressiva do tempo.

## Funções Principais

### `countDown()`

Esta função é responsável por diminuir o tempo restante e atualizar o elemento de exibição do tempo. Quando o tempo chega a zero, ela limpa os intervalos e exibe uma mensagem de "Game Over" com a pontuação do jogador.

### `playSound(audioName)`

Esta função reproduz um som quando o jogador clica no quadrado inimigo. Ela cria um elemento de áudio e ajusta o volume antes de iniciar a reprodução.

### `randomSquare()`

Esta função remove a classe "enemy" de todos os quadrados, escolhe aleatoriamente um quadrado para ser o inimigo e adiciona a classe "enemy" a ele. Ela também atualiza a posição do quadrado inimigo no estado.

### `addListenerHitBox()`

Esta função adiciona um evento de clique a cada quadrado do jogo. Quando um quadrado é clicado, ela verifica se é o quadrado inimigo correto e, se for, aumenta a pontuação do jogador e reproduz um som.

### `init()`

A função `init()` é chamada para iniciar o jogo. Ela configura os ouvintes de clique nos quadrados e começa os intervalos para a geração aleatória do inimigo e a contagem regressiva do tempo.

## Como Jogar

- Clique no quadrado inimigo sempre que ele aparecer para ganhar pontos.
- Tente marcar o máximo de pontos possível antes que o tempo acabe.
- Quando o tempo chegar a zero, você verá sua pontuação final em um alerta.


## Créditos
- Este jogo foi desenvolvido como parte de um projeto educacional da Digital Innovation One.



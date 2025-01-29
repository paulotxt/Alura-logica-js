# Jogo do Número Secreto - Projeto de Estudo de Lógica de Programação

Este repositório contém um projeto simples de estudo de lógica de programação em JavaScript. O objetivo é criar um jogo onde o usuário tenta adivinhar um número secreto gerado aleatoriamente.

## Descrição do Projeto

O jogo consiste em adivinhar um número secreto gerado aleatoriamente entre 1 e um número máximo definido. O usuário recebe dicas se o número secreto é maior ou menor que o número escolhido. O jogo continua até que o usuário adivinhe o número correto, e o número de tentativas é exibido ao final.

## Como Funciona

1. O jogo começa exibindo uma mensagem de boas-vindas.
2. Um número secreto é gerado aleatoriamente entre 1 e o número máximo definido (50, neste caso).
3. O usuário é solicitado a escolher um número dentro do intervalo.
4. Se o número escolhido for igual ao número secreto, o jogo termina e o número de tentativas é exibido.
5. Se o número escolhido for maior ou menor que o número secreto, o usuário recebe uma dica e o jogo continua.
6. O jogo termina quando o usuário adivinha o número secreto, e o número de tentativas é exibido.

## Código

```javascript
alert('Boas vindas ao jogo do número secreto');
let numeroMaximo = 50;
let numeroSecreto = parseInt(Math.random() * numeroMaximo + 1);
console.log(numeroSecreto);
let chute;
let tentativas = 1;

while (chute != numeroSecreto) {
    chute = prompt(`Escolha um número entre 1 a ${numeroMaximo}`);

    if (chute == numeroSecreto) {
        break;
    } else {
        if (chute > numeroSecreto) {
            alert(`O número secreto é menor que ${chute}`);
        } else {
            alert(`O número secreto é maior que ${chute}`);
        }
        tentativas++;
    }
}

let palavraTentativa = tentativas > 1 ? 'tentativas' : 'tentativa';
alert(`Isso aí! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} ${palavraTentativa}`);
```

## Como Executar

1. Clone este repositório.
2. Abra o arquivo `index.html` em um navegador web.
3. Siga as instruções exibidas na tela para jogar.

## Contribuição

Este projeto é destinado a fins educacionais. Se você quiser contribuir ou sugerir melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

---

Divirta-se jogando e aprendendo lógica de programação! 🎉

# Teste de PSI 1 - Turno 2 - Versão 2

## Informação do aluno

    Nome: ...

Teste termina às 13:25.

Escreve as respostas dentro dos blocos correspondentes.
Substitui as reticências pelo que é pedido em cada pergunta.
Não desformates o documento.

### P1. Indica o que é impresso pelo seguinte código. Justifica a tua resposta

    ulong uL = ulong.MaxValue;

    Console.WriteLine(uL + 1);

P1 - Resposta

    É impresso: 0

    A propriedade 'MaxValue' corresponde ao valor máximo de um determinado tipo.
    Neste caso, estamos a guardar o valor máximo de 'unsigned long' numa variável do mesmo tipo.
    O método Console.WriteLine é responsável por imprimir um tipo de valor. 
    Este valor é passado entre parênteses depois do nome do método.
    Assim sendo, vai ser impresso o valor 'uL + 1'.
    Sendo que estamos a incrementar uma variável do tipo 'unsigned long' que já tem o valor máximo deste tipo,
    irá ocorrer "overflow", o que faz com que o valor de 'uL' "dê a volta",
    e volte ao valor mínimo deste tipo, que é 0.

### P2. Considera o seguinte código com um *bug*

    float f = double.MaxValue;

    Console.WriteLine(f);

### Indica uma possível correção para que o código não apresente erros. Explica porque foi necessário fazer essa correção

P2 - Resposta

    Uma possível correção: float f = float.MaxValue;

    A propriedade 'MaxValue' corresponde ao valor máximo de um determinado tipo.
    Neste caso, estamos a tentar guardar o valor máximo de 'double' numa variável 'float'.
    Visto que 'float' tem um alcançe inferior a 'double', é impossível a variável 'f' guardar o valor pedido.
    Assim sendo, podemos alterar o tipo a que a propriedade 'MaxValue' acede para 'float'.

### P3. Escreve um programa que solicite ao utilizador dois números reais e apresente o resultado do segundo (base) elevado ao primeiro (expoente). Não podes usar um método da classe Math para obter o resultado

P3 - Resposta

    // Variáveis para guardar números reais e resultado da operação
    float b, e, resultado = 1.0f;

    // Pedir o primeiro número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o primeiro número real: ");
    e = Convert.ToSingle(Console.ReadLine());

    // Pedir o segundo número ao utilizador e guardar na variável correspondente
    Console.Write("Insere o segundo número real: ");
    b = Convert.ToSingle(Console.ReadLine());

    // Ciclo FOR para calcular número base elevado ao número expoente
    for (int i = 0; i < e; i++)
    {
      // Multiplicar número base 'e' vezes e guardar resultado na variável correspondente
      resultado *= b;
    }

    // Imprimir resultado da soma
    Console.WriteLine($"{b} elevado a {e} = {resultado}");

### P4. Estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'Perks.cs'. Queres enviar **apenas** esta atualização para o teu repositório remoto. Indica os comandos necessários. A mensagem de commit deve ser apropriada

P4 - Resposta

    1. Adicionar ficheiro 'Perks.cs' para commit
        git add Classes.cs

    2. Fazer commit com mensagem apropriada
        git commit -m "Atualizar ficheiro Perks.cs"

    3. Enviar atualização para o repositório remoto
        git push

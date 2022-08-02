# Passando-Vetores-e-Matrizes-para-Metodos-Cod-Java-
Ir para o conteúdo principal
Damares Costa de Souza 
Moodle - IFRS

Programação Básica com Java III - Turma 2022B
Painel Meus cursos  PBJIII2022B 4. Procedimentos, Funções e Métodos  4.10. Passando Vetores e Matrizes para Métodos
4.10. Passando Vetores e Matrizes para Métodos
Nesta última seção vamos nos concentrar na linguagem Java. A passagem de vetores e matrizes como parâmetro em pseudocódigo não apresenta nenhuma novidade em relação a declaração de variáveis e ao que será explicado em Java abaixo.

Para passar um vetor como argumento para um método, especifique o nome do vetor sem nenhum colchete. Por exemplo, se o arranjo temperaturasPorDia é declarado como

int temperaturasPorDia[] = new int[30];

a chamada de método

modificaVetor( temperaturasPorDia );

passa o vetor temperaturasPorDia para o método modificaVetor.
Para um método receber um vetor como parâmetro, a lista de parâmetros dele deve conter uma especificação de vetor (ou várias, se mais de um vetor deve ser recebido). Por exemplo, o cabeçalho do método modificavetor poderia ser escrito assim:

static void modificaVetor( int b[] )

indicando que o método espera receber um vetor de inteiros no parâmetro b.
O código abaixo ilustra a passagem de vetores para métodos. A saída do programa é mostrada logo a seguir.



1      public class PassagemPorReferencia {

2            static void modificaVetor( int b[] ) {

3                   for(int cont = 0; cont < b.length; cont++ )

4                          b[cont] *= 2;

5            }

6

7            public static void main(String[] args) {

8                   int[] numeros = { 1, 2, 3, 4, 5 };

9

10                  System.out.print(“Valores originais: ”);

11                  for(int pos = 0; pos < 5; pos++)

12                         System.out.println(numeros[pos] + “ ”);

13

14                  modificaVetor( numeros );

15

16                  System.out.print(“Valores modificados: ”);

17                  for(int pos = 0; pos < 5; pos++)

18                         System.out.println(numeros[pos] + “ ”);

19

20           }

21     }


Imagem mostra o seguinte texto: Valores originais...: 1 2 3 4 5 Valores modificados.: 2 4 6 8 10

Note que, após a chamada ao método modificaVetor, o conteúdo da variável numeros foi modificado. Isso aconteceu, porque o arranjo foi passado por referência. Todas as modificações feitas no parâmetro b foram também realizadas na variável numeros. Note também a linha 3. Nessa linha é utilizado um atributo especial de todos os vetores em Java chamado length. Esse atributo contém o número de elementos do arranjo. No caso do exemplo, a chamada devolveria 5, o número de elementos do arranjo numeros. Lembre-se que para fazer uso do atributo length, basta escrever o nome da variável que contém o vetor seguido de um ponto final e da palavra length.

Última atualização: domingo, 1 nov 2020, 20:50
Seguir para...
Academi
Dúvidas? 
Perguntas frequentes

Fale conosco | Suporte | Contato

Informação
Termos e Condições de Uso
Aviso de Privacidade e Proteção de Dados Pessoais
Contato
Rua Gen. Osório, 348, Bento Gonçalves/RS
Siga-nos
Copyright © 2017 - Desenvolvido por LMSACE.com. Distribuído por Moodle

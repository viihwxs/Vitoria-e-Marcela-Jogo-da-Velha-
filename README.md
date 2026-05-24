//Vitoria Luisa Moreira Amaral e Marcela Reis 
programa
{
	
	funcao vazio jogar()
{
	caracter tabuleiro[3][3]
	caracter posicao
	inteiro linha, coluna
	inteiro jogador = 0
	inteiro jogadas = 0
	
	
	para(inteiro i = 0; i < 3; i++)
	{
		para(inteiro j = 0; j < 3; j++)
		{
			tabuleiro[i][j] = '-'
		}
	}
	
	enquanto(jogadas < 9)
	{
		
		
		escreva("linha 1  ", tabuleiro[0][0], "  ", tabuleiro[0][1], "  ", tabuleiro[0][2], "\n")
		escreva("linha 2 ", tabuleiro[1][0], "  ", tabuleiro[1][1], "  ", tabuleiro[1][2], "\n")
		escreva("linha 3  ", tabuleiro[2][0], "  ", tabuleiro[2][1], "  ", tabuleiro[2][2], "\n")
		
		escreva("\nJogador ", jogador, " escolha uma posicao (de 1 a 9): ")
		leia(posicao)
		
		escolha(posicao)
		{
			caso '1': linha = 0
					coluna = 0
					pare
					
			caso '2': linha = 0
					coluna = 1
					pare
					
			caso '3': linha = 0
					coluna = 2
					pare
					
			caso '4': linha = 1
					coluna = 0
					pare
					
			caso '5': linha = 1
					coluna = 1
					pare
					
			caso '6': linha = 1
					coluna = 2
					pare
					
			caso '7': linha = 2
					coluna = 0
					pare
					
			caso '8': linha = 2
					coluna = 1
					pare
					
			caso '9': linha = 2
					coluna = 2
					pare
			
			caso contrario:
				escreva("Posicao invalida!\n")
				
		}
		
	
		se(tabuleiro[linha][coluna] != '-')
		{
			escreva("Posicao ja ocupada!\n")
			
		}
		
		
		se(jogador == 0)
		{
			tabuleiro[linha][coluna] = '0'
			jogador = 1
		}
		senao
		{
			tabuleiro[linha][coluna] = '1'
			jogador = 0
		}
		
		jogadas++
	}
	
	escreva("\nFim do jogo!\n")
}

funcao inicio()
	{
		inteiro opcao
		
		faca
		{
			escreva("\nMENU \n")
			escreva("1 - Jogar\n")
			escreva("2 - placar\n")
			escreva("3 - Sair\n")
			escreva("Escolha uma opcao: ")
			leia(opcao)
			
			escolha(opcao)
			{
				caso 1:
					jogar()  
					pare
					
				caso 2:
					escreva("\nMostrando placar...\n")
					pare
					
				caso 3:
					escreva("\nJogo Encerrado...\n")
					pare
					
				caso contrario:
					escreva("\nOpcao invalida!\n")
			}
			
		} enquanto(opcao != 3)
	}
}

    
    /*Professor, conseguimos fazer boa parte do trabalho, como o menu e a parte do jogo usando matriz e laço de repetição, igual foi pedido. O jogo já funciona para dois jogadores, deixando escolher as posições e marcando certinho no tabuleiro com 0 e 1.

    Mas ainda não conseguimos terminar tudo. A parte de verificar vitória (linha, coluna e diagonal) não deu tempo de finalizar, então o jogo ainda não mostra quem ganhou. Também tivemos dificuldade para fazer o placar continuar funcionando entre as partidas sem usar variável global.

    Além disso, algumas entradas inválidas ainda podem dar erro, tipo quando escolhe uma posição que já está ocupada.

    Mesmo assim, o código mostra os conteúdos pedidos na atividade, como matriz, funções, repetição e controle de fluxo. /*


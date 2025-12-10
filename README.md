# Batalha-Naval-b-sico
#include <stdio.h>

#define TAMANHO_TABULEIRO 10
#define TAMANHO_NAVIO 3

// Função para exibir o tabuleiro
void exibirTabuleiro(int tabuleiro[TAMANHO_TABULEIRO][TAMANHO_TABULEIRO]) {
    for (int i = 0; i < TAMANHO_TABULEIRO; i++) {
        for (int j = 0; j < TAMANHO_TABULEIRO; j++) {
            printf("%d ", tabuleiro[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int tabuleiro[TAMANHO_TABULEIRO][TAMANHO_TABULEIRO] = {0}; // Inicializa o tabuleiro com água (0)
    
    // Definir e posicionar os navios diretamente (sem validações extras)
    
    // Navio 1 (horizontal) - posição na linha 2, coluna 3
    int linha1 = 2, coluna1 = 3;
    for (int i = 0; i < TAMANHO_NAVIO; i++) {
        tabuleiro[linha1][coluna1 + i] = 3; // Marca as posições do navio 1
    }
    
    // Navio 2 (vertical) - posição na linha 5, coluna 7
    int linha2 = 5, coluna2 = 7;
    for (int i = 0; i < TAMANHO_NAVIO; i++) {
        tabuleiro[linha2 + i][coluna2] = 3; // Marca as posições do navio 2
    }
    
    // Exibir o tabuleiro
    printf("\nTabuleiro de Batalha Naval:\n");
    exibirTabuleiro(tabuleiro);

    return 0;
}

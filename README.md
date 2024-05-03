#include <iostream>
#include <vector>

using namespace std;

// Função para converter um número inteiro para binário
vector<int> intToBinary(int n) {
    vector<int> binary;
    
    // Caso base: se o número for zero, retorna um vetor com apenas um elemento zero
    if (n == 0) {
        binary.push_back(0);
        return binary;
    }
    
    // Enquanto o número não for zero, continua dividindo por 2 e armazenando os restos
    while (n > 0) {
        binary.push_back(n % 2);
        n /= 2;
    }
    
    // Inverte o vetor para obter a representação binária correta
    (binary.begin(), binary.end());
    
    return binary;
}

int main() {
    int num;
    cout << "Digite um número inteiro: ";
    cin >> num;

    vector<int> binary = intToBinary(num);

    cout << "O número " << num << " em binário é: ";
    for (int bit : binary) {
        cout << bit;
    }
    cout << endl;

    return 0;
}

# Controle da Impressora Térmica Elgin i8/i9 em C

## O que o programa faz
Programa em C (arquivo `main.c`) que pede login e mostra um menu para controlar uma impressora Elgin i8 ou i9 usando a DLL `E1_Impressora01.dll`: imprime texto, QR Code, código de barras, XML SAT e cancelamento SAT, abre a gaveta e emite sinal sonoro.

## Como compilar e executar
1. Coloque na mesma pasta: `main.c`, `E1_Impressora01.dll`, `XMLSAT.xml` e `CANC_SAT.xml`.
2. Descubra os bits do compilador: `gcc -dumpmachine`
   - `x86_64-w64-mingw32` (64 bits) → use a DLL da pasta **x64**
   - `mingw32` / `i686-w64-mingw32` (32 bits) → use a DLL da pasta **x86**
3. Compile e execute:
```
gcc main.c -o impressora.exe
impressora.exe
```
4. Ligue a impressora e conecte o cabo USB antes de testar.

## Login de teste
- Usuário: `admin`
- Senha: `1234`
(3 tentativas)

## Opções do menu
| Nº | Opção |
|----|-------|
| 1 | Configurar conexão (USB: tipo 1, modelo i9, porta USB, parâmetro 0) |
| 2 | Abrir conexão |
| 3 | Fechar conexão |
| 4 | Imprimir texto |
| 5 | Imprimir QR Code |
| 6 | Imprimir código de barras |
| 7 | Imprimir XML SAT |
| 8 | Imprimir XML de cancelamento SAT |
| 9 | Abrir gaveta (Elgin) |
| 10 | Abrir gaveta |
| 11 | Sinal sonoro |
| 0 | Sair |

## Autores
- Matheus Henrique Lima da Silva
- (adicione os outros integrantes do grupo)

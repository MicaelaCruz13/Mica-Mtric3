# Mica-Mtric3
Ejercicio de matrices
```C

#include <stdlib.h>
#include <time.h>

int main(){
    int b = 1;
    char opcion;
    int puntos=0;
    int carta;
    
    while(b=1){
        printf("Adivine la siguiente carta \n A_Alta\n B_Baja\n");
        scanf("%s",&opcion);
        opcion = tolower(opcion);
        srand(time(NULL)); 
        carta=rand() % 14;
        
        if (carta==7){
            printf("Carta %d\nPerdiste!\n;",carta);
            break;
        }else if (carta < 7){
            if(opcion == 'b'){
            (puntos == 0) ? (puntos = 2) : (puntos = puntos);    
            puntos = puntos * 2;
            printf("Baja %d\nTenes %d Puntos\n",carta,puntos);
            }else{
                printf("Baja %d\n",carta);
                break;
            }
        }else if (carta > 7){
            if(opcion == 'a'){
            (puntos == 0) ? (puntos = 2) : (puntos = puntos);    
            puntos = puntos * 2;
            printf("Alta %d\nTenes %d Puntos\n",carta,puntos);
            }else{
                printf("Alta %d\n",carta);
                break;
            }
        }
    }
    printf("Juego Terminado \nPuntos: %d\nCarta %d\n",puntos,carta);
    return 0;
}
```

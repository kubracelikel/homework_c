#include <stdio.h>
#include <stdlib.h>
#include <time.h>

#define SATIR_A 2
#define SUTUN_A 3

#define SATIR_B 3
#define SUTUN_B 2

int matrisA[SATIR_A][SUTUN_A];
int matrisB[SATIR_B][SUTUN_B];

void rastgeleMatrisUret(int satir, int sutun, int matris[satir][sutun]);

void matrisYazdir(int satir, int sutun, int matris[satir][sutun]);

void matrisTopla(int a[SATIR_A][SUTUN_A], int b[SATIR_B][SUTUN_B]);

void matrisCarp(int a[SATIR_A][SUTUN_A], int b[SATIR_B][SUTUN_B]);

int main() {
    srand(time(NULL));

    printf("\n*** A Matrisi ***\n");
    rastgeleMatrisUret(SATIR_A, SUTUN_A, matrisA);
    matrisYazdir(SATIR_A, SUTUN_A, matrisA);

    printf("\n*** B Matrisi ***\n");
    rastgeleMatrisUret(SATIR_B, SUTUN_B, matrisB);
    matrisYazdir(SATIR_B, SUTUN_B, matrisB);

    printf("\n*** Matris Toplami ***\n");
    if (SATIR_A != SATIR_B || SUTUN_A != SUTUN_B) printf("Matris boyutlari uyumsuz. Toplama islemi yapilamaz.\n");
    else matrisTopla(matrisA, matrisB);

    printf("\n*** Matris Carpimi ***\n");
    if (SUTUN_A != SATIR_B) printf("Matris boyutlari uyumsuz. Carpma işlemi yapilamaz.\n");
    else matrisCarp(matrisA, matrisB);

    return 0;
}

void rastgeleMatrisUret(int satir, int sutun, int matris[satir][sutun]) {
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            matris[i][j] = rand() % 100 + 1;
        }
    }
}

void matrisYazdir(int satir, int sutun, int matris[satir][sutun]) {
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            printf("%d ", matris[i][j]);
        }

        printf("\n");
    }
}

void matrisTopla(int a[SATIR_A][SUTUN_A], int b[SATIR_B][SUTUN_B]) {
    int sonuc[SATIR_A][SUTUN_A];

    for (int i = 0; i < SATIR_A; i++) {
        for (int j = 0; j < SUTUN_A; j++) {
            sonuc[i][j] = a[i][j] + b[i][j];
        }
    }

    matrisYazdir(SATIR_A, SUTUN_A, sonuc);
}

void matrisCarp(int a[SATIR_A][SUTUN_A], int b[SATIR_B][SUTUN_B]) {
    int sonuc[SATIR_A][SUTUN_B];

    for (int i = 0; i < SATIR_A; i++) {
        for (int j = 0; j < SUTUN_B; j++) {
            sonuc[i][j] = 0;
            for (int k = 0; k < SUTUN_A; k++) {
                sonuc[i][j] += a[i][k] * b[k][j];
            }
        }
    }

    matrisYazdir(SATIR_A, SUTUN_B, sonuc);
}

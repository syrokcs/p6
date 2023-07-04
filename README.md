#include <stdio.h>
#include <math.h>

double find_vector_length(int x1, int y1, int x2, int y2) {
    double length = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));
    return round(length * 1000000) / 1000000;  // Округлюємо до шести знаків після коми
}

int main() {
    int x1, y1, x2, y2;

    printf("Введіть координату x1: ");
    scanf("%d", &x1);
    printf("Введіть координату y1: ");
    scanf("%d", &y1);
    printf("Введіть координату x2: ");
    scanf("%d", &x2);
    printf("Введіть координату y2: ");
    scanf("%d", &y2);

    double vector_length = find_vector_length(x1, y1, x2, y2);

    printf("Довжина вектора: %.6lf\n", vector_length);

    return 0;
}

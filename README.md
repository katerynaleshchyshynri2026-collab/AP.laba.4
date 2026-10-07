# AP.laba.4
#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    int N, i;
    double P;

    cout << "N = "; cin >> N;

    // 1) while
    P = 1;
    i = N;
    while (i <= 10)
    {
        P *= (i + 1. / (i * i)) / sqrt(1 + exp(1. / i));
        i++;
    }
    cout << P << endl;

    // 2) do-while
    P = 1;
    i = N;
    do {
        P *= (i + 1. / (i * i)) / sqrt(1 + exp(1. / i));
        i++;
    } while (i <= 10);
    cout << P << endl;

    // 3) for (i збільшується)
    P = 1;
    for (i = N; i <= 10; i++)
    {
        P *= (i + 1. / (i * i)) / sqrt(1 + exp(1. / i));
    }
    cout << P << endl;

    // 4) for (i зменшується, від 10 до N)
    P = 1;
    for (i = 10; i >= N; i--)
    {
        P *= (i + 1. / (i * i)) / sqrt(1 + exp(1. / i));
    }
    cout << P << endl;

    return 0;
}

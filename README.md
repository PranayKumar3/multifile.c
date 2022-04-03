#include "stdio.h"
#include "complex.h"
#include "complex.h"

complex_t complex_sum(complex_t c1, complex_t c2)
{
    complex_t sol;
    sol.real = c1.real + c2.real;
    sol.img = c1.img + c2.img;
    return sol;
}
complex_t complex_difference(complex_t c1, complex_t c2)
{
    complex_t sol;
    sol.real = c1.real - c2.real;
    sol.img = c1.img - c2.img;
    return sol;
}
complex_t complex_multiply(complex_t c1, complex_t c2)
{
    complex_t sol;
    sol.real = c1.real * c2.real - c1.img * c2.img;
    sol.img = c1.img * c2.real + c1.real * c2.img;
    return sol;
}
complex_t complex_divide(complex_t c1, complex_t c2)
{
    complex_t sol;

    sol.real = ((c1.real * c2.real) + (c1.img * c2.img)) / ((c2.real * c2.real) + (c2.img * c2.img));
    sol.img = ((c1.img * c2.real) - (c1.real * c2.img)) / ((c2.real * c2.real) + (c2.img * c2.img));
    return sol;
}

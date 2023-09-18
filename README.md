#include <iostream>

using namespace std;

double func(double x)
{
	double res = (x + 1) / sqrt(pow(x, 2) + 2);
	return res;
}
double left_rect(double a, double b, int n)
{
	double h = (b - a) / n;
	double s = 0;
	double xb = a;
	for (int i = 0; i <= n-1; i++)
	{
		double x = xb + i * h;
		s = s + h * func(x);
	}
	return s;
}

double right_rect(double a, double b, int n)
{
	double h = (b - a) / n;
	double s = 0;
	double x = a +h;
	while (x <= b)
	{
		double y = func(x);
		s = s + y;
		x = x + h;
	}
	s = s * h;
	return s;
}

double middle_rect(double a, double b, int n)
{
	double h;
	h = (b - a) / n;
	double S = 0;
	for(int i = 1; i <= n; i ++)
	{
		S = S + func(a + (i - 0.5) * h);
	}
	double I = h * S;
	return I;
}
double nuton_lebnic(double a, double b)
{
	return func(b) - func(a);
}

int main()
{
	setlocale(LC_ALL, "RUS");
	double r_res_n10 = right_rect(1.6, -0.4, 10);
	double r_res_n50 = right_rect(1.6, -0.4, 50);
	double r_res_n100 = right_rect(1.6, -0.4, 100);
	cout << "Метод правых прямоугольников при n = 10 - ";
	cout << r_res_n10;
	cout << endl;
	cout << "Метод правых прямоугольников при n = 50 - ";
	cout << r_res_n50;
	cout << endl;
	cout << "Метод правых прямоугольников при n = 100 - ";
	cout << r_res_n100;
	cout << endl;
	double l_res_n10 = left_rect(1.6, -0.4, 10);
	double l_res_n50 = left_rect(1.6, -0.4, 50);
	double l_res_n100 = left_rect(1.6, -0.4, 100);
	cout << "Метод левых прямоугольников при n = 10 - ";
	cout << l_res_n10;
	cout << endl;
	cout << "Метод левых прямоугольников при n = 50 - ";
	cout << l_res_n50;
	cout << endl;
	cout << "Метод левых прямоугольников при n = 100 - ";
	cout << l_res_n100;
	cout << endl;
	double s_res_n10 = middle_rect(1.6, -0.4, 10);
	double s_res_n50 = middle_rect(1.6, -0.4, 50);
	double s_res_n100 = middle_rect(1.6, -0.4, 100);
	cout << "Метод средних прямоугольников при n = 10 - ";
	cout << s_res_n10;
	cout << endl;
	cout << "Метод средних прямоугольников при n = 50 - ";
	cout << s_res_n50;
	cout << endl;
	cout << "Метод средних прямоугольников при n = 100 - ";
	cout << s_res_n100;
	cout << endl;
	double res_n_l = nuton_lebnic(1.6, -0.4);
	cout << "Ньютона Лейпница - ";
	cout << res_n_l;
	
	


}#include <iostream>

using namespace std;

double func(double x)
{
	double res = (x + 1) / sqrt(pow(x, 2) + 2);
	return res;
}
double left_rect(double a, double b, int n)
{
	double h = (b - a) / n;
	double s = 0;
	double xb = a;
	for (int i = 0; i <= n-1; i++)
	{
		double x = xb + i * h;
		s = s + h * func(x);
	}
	return s;
}

double right_rect(double a, double b, int n)
{
	double h = (b - a) / n;
	double s = 0;
	double x = a +h;
	while (x <= b)
	{
		double y = func(x);
		s = s + y;
		x = x + h;
	}
	s = s * h;
	return s;
}

double middle_rect(double a, double b, int n)
{
	double h;
	h = (b - a) / n;
	double S = 0;
	for(int i = 1; i <= n; i ++)
	{
		S = S + func(a + (i - 0.5) * h);
	}
	double I = h * S;
	return I;
}
double nuton_lebnic(double a, double b)
{
	return func(b) - func(a);
}

int main()
{
	setlocale(LC_ALL, "RUS");
	double r_res_n10 = right_rect(1.6, -0.4, 10);
	double r_res_n50 = right_rect(1.6, -0.4, 50);
	double r_res_n100 = right_rect(1.6, -0.4, 100);
	cout << "Метод правых прямоугольников при n = 10 - ";
	cout << r_res_n10;
	cout << endl;
	cout << "Метод правых прямоугольников при n = 50 - ";
	cout << r_res_n50;
	cout << endl;
	cout << "Метод правых прямоугольников при n = 100 - ";
	cout << r_res_n100;
	cout << endl;
	double l_res_n10 = left_rect(1.6, -0.4, 10);
	double l_res_n50 = left_rect(1.6, -0.4, 50);
	double l_res_n100 = left_rect(1.6, -0.4, 100);
	cout << "Метод левых прямоугольников при n = 10 - ";
	cout << l_res_n10;
	cout << endl;
	cout << "Метод левых прямоугольников при n = 50 - ";
	cout << l_res_n50;
	cout << endl;
	cout << "Метод левых прямоугольников при n = 100 - ";
	cout << l_res_n100;
	cout << endl;
	double s_res_n10 = middle_rect(1.6, -0.4, 10);
	double s_res_n50 = middle_rect(1.6, -0.4, 50);
	double s_res_n100 = middle_rect(1.6, -0.4, 100);
	cout << "Метод средних прямоугольников при n = 10 - ";
	cout << s_res_n10;
	cout << endl;
	cout << "Метод средних прямоугольников при n = 50 - ";
	cout << s_res_n50;
	cout << endl;
	cout << "Метод средних прямоугольников при n = 100 - ";
	cout << s_res_n100;
	cout << endl;
	double res_n_l = nuton_lebnic(1.6, -0.4);
	cout << "Ньютона Лейпница - ";
	cout << res_n_l;
	
	


}

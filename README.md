## Welcome to my dev blog

Hello. My name is Rodrigo. I am from Brazil and here you can find my personal works I have been doing with game programming.
My last works are targeting mainly in Unreal game engine and game engine programming.

I have been working since June last year in two different projects. A game demo project in Unreal Engine and in my own game engine to brush up my skills in C++ and computer graphics techniques. Both projects will help me to show off my skills in gaming technologies as I am aiming to work in game companies soon.

## Which step am I right now?
### Math Library

My last studies are in developing a math library to be used in the rain forest engine. It will feature math game programming related functions such as operations in vectors, matrices and quaternions.

I start with a Vector class that will represent a Vector, of course, in the library. Basic constructor and override constructors with diferent parameters to make it flexible enough.

```c++
class rfVector3
{
public:

	// constructors
	rfVector3();
	rfVector3(double x, double y, double z);
	rfVector3(const rfVector3& _vector);
	~rfVector3();
```

I will feature main operations line Addition, Subtraction and scalar multiplication. For that, I take advantage of operator overloading features of C++ that does this work to me. I simply create static functions that I need to pass vectors as arguments that will be affected by the operation.

```c++
rfVector3& rfVector3::Addition(const rfVector3& vector, const rfVector3& otherVector)
{
	return *new rfVector3(vector.operator+(otherVector));
}

rfVector3& rfVector3::Subtraction(const rfVector3& vector, const rfVector3& otherVector)
{
	return *new rfVector3(vector.operator-(otherVector));
}

rfVector3& rfVector3::Scalar(const rfVector3& vector, const double scalar)
{
	return *new rfVector3(vector.operator*(scalar));
}
```
[Imgur](https://i.imgur.com/pGvfKR9.png)
Vector Operations

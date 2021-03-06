<h1 align="center">LambdaExpression</h1>
<h2>Lambda Expression is also called an anonymous function,  is a defined function not bound to an identifier.</h2>

<h2>Syntax of Lambda expressions:</h2>

```
(argument-list) -> {body}
```
<h2>Lambda expression in java consists of the following 3 components:</h2>

* Argument-list: parameter list, possibly none, with one or more parameters.

* Arrow-operator: the arrow operator is used to bind the parameter list and the body of the expression.

* Body: executable content, is a block of code or an expression.

<h2>Lambda Expression Example:</h2>

* No parameters:

```java
@FunctionalInterface
interface HelloWorld {
    public String helloWorld();
}

public class LambdaExpression {
    public static void main(String[] args) {
        HelloWorld helloWorld = () -> {
            return "Hello World.";
        };
        System.out.println(s.helloWorld());
    }
}
```

* There is 1 parameter:

```java
@FunctionalInterface
interface HelloWorld {
    public String helloWorld(String message);
}

public class LambdaExpression {
    public static void main(String[] args) {
        HelloWorld helloWorld = message -> "Hello " + message;
        System.out.println(s.sayHello("World."));
    }
}
```

* There are many parameters:

```java
@FunctionalInterface
interface SumIntegers {
    Integer sumIntegers(int ...args);
}
public class LambdaExpression {
    public static void main(String[] args) {
        SumIntegers sumIntegers = integers -> {
            Integer result = 0;
            for(int i = 0;i<integers.length;i++ ){
                result += integers[i];
            }
            return result;
        };
        Integer sum = lambdaExpression.sumIntegers.sumIntegers(12,2,2,34,5,3,3,1,2);
        System.out.println("Sum of Integers: "+ sum);
    }
}
```
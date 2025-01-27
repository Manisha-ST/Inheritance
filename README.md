# Inheritance
package shapeinheritance;

abstract class Shape{
    public abstract double calculateArea();
    }
class Circle extends Shape{
    private double radius;
    public Circle(double radius){
        this.radius=radius;
    }
  
public double calculateArea(){
    return Math.PI*radius*radius;
}
}
class Rectangle extends Shape{
    private double length,width;
    public Rectangle(double length,double width){
        this.length=length;
        this.width=width;
    }
    public double calculateArea(){
    return length*width;
}
}
class Square extends Shape{
    private double side;
    public Square(double side){
        this.side=side;
    }
    public double calculateArea(){
        return side*side;
    }
}
class Triangle extends Shape{
    private double base,heigth;
    public Triangle(double base,double heigth){
        this.base=base;
        this.heigth=heigth;
    }
    public double calculateArea(){
        return 0.5*base*heigth;
    }
}

public class Shapeinheritance{
    public static void main(String[]args){
        Shape circle=new Circle(5);
        Shape rectangle = new Rectangle(4, 6);
        Shape square = new Square(4);
        Shape triangle = new Triangle(3, 5);
        
System.out.println("Circle area:"+circle.calculateArea());
System.out.println("Rectangle Area:" + rectangle.calculateArea());
System.out.println("Square Area:"+square.calculateArea());
System.out.println("Triangle Area:"+triangle.calculateArea());
    }
}

Output:
Circle area:78.53981633974483
Rectangle Area:24.0
Square Area:16.0
Triangle Area:7.5

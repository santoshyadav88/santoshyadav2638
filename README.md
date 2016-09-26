# santoshyadav2638
//Reflection example how to get info about assembly during runtime.
public class MyClass
{
    public virtual int Add(int numb1, int numb2)
    {                
        return numb1 + numb2;
    }
    public virtual int Subtract(int numb1, int numb2)
    {
        return numb1 - numb2;
    }
}

static void Main(string[] args)
{
    MyClass oMyClass = new MyClass();
    //Type information.
    Type oMyType = oMyClass.GetType();
    //Method information.
    MethodInfo oMyMethodInfo = oMyType.GetMethod("Subtract");

    Console.WriteLine("\nType information:" + oMyType.FullName);
    Console.WriteLine("\nMethod info:" + oMyMethodInfo.Name);            
    Console.Read();
}

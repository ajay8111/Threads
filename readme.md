## Threads In Java

### Threads
- A Thread is a light weight procces in java used for multitasking.
- Java Threads are managed by JVM (Java Virtual Machines).
- Threads allows program to run multiple tasks simultaneously.
- Threads are created by extending Thread class.

### Example of creating a thread

```java


class Example extends Thread {
    public void run() 
    {
        System.out.println("New Thread is started.."); 
        
    }
}

class Main {
    public static void main(String args[]){
        Example t1 = new Example();
        t1.start();
        System.out.println("Primary Thread.");

        
    }
}


```

- run() method is used to run the thread in main 
- start() is used to create a new thread


## Multiple Threads

Instead of single thread, multiple threads run simultaneously to improve performance and efficiency.
Multi-Thread allows multiple part of the program to run at the same time.

### Example of multithread

```java
class A extends Thread{
   public void run()
   {
       for(int i=0;i<=5;i++){
           System.out.println("Hi");
       }
   }
    
}

class B extends Thread{
    
    public void run()
   {
       for(int i=0;i<=5;i++){
           
           System.out.println("Hello");
       }
   }
}

class Main{
    public static void main(String args[]){
        A t1 = new A();
        B t2 = new B();
        
        t1.start();
        t2.start();

    }
}

```

## Thread Priority and Sleep


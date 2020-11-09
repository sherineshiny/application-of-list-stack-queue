public class Queue{
 int size=5;
 int items[]=new int[size];
 int front,rear;
 Queue(){
 front=-1;
 rear=-1;
 }
 boolean isFull(){
   if(front==0&&rear==size-1){
    return true;
    }
    return false;
   }
   boolean isEmpty(){
     if(front==-1)
      return true;
     else
      return false;
     }
     void enQueue(int element){
      if(isFull()){
        System.out.println("queue is full");
        }else{
          if(front==-1)
             front=0;
             rear++;
             items[rear]=element;
             System.out.println("inserted"+element);
            }
           } 
     int deQueue() {
    int element;
    if (isEmpty()) {
      System.out.println("Queue is empty");
      return (-1);
    } else {
      element = items[front];
      if (front >= rear) {
        front = -1;
        rear = -1;        
         } 
       else {
        front++;
      }
      System.out.println("Deleted -> " + element);
      return (element);
    }
  }
  void display() {
   int i;
    if (isEmpty()) {
      System.out.println("Empty Queue");
    } else {
      System.out.println("\nFront index-> " + front);
      System.out.println("Items -> ");
      for (i = front; i <= rear; i++)
        System.out.print(items[i] + "  ");
      System.out.println("\nRear index-> " + rear);
    }
  }
  class Stack { 
    static final int MAX = 1000; 
    int top; 
    int a[] = new int[MAX]; // Maximum size of Stack 
  boolean isEmpty() 
    { 
        return (top < 0); 
    } 
    Stack() 
    { 
        top = -1; 
    } 
  boolean push(int x) 
    { 
        if (top >= (MAX - 1)) { 
            System.out.println("Stack Overflow"); 
            return false; 
        } 
        else { 
            a[++top] = x; 
            System.out.println(x + " pushed into stack"); 
            return true; 
        } 
    } 
  
  int pop() 
    { 
        if (top < 0) { 
            System.out.println("Stack Underflow"); 
            return 0; 
        } 
        else { 
            int x = a[top--]; 
            return x; 
        } 
    } 
    int peek() 
    { 
        if (top < 0) { 
            System.out.println("Stack Underflow"); 
            return 0; 
        } 
        else { 
            int x = a[top]; 
            return x; 
        } 
    } 
} 
class Book {  
int id;  
String name,author,publisher;  
int quantity;  
public Book(int id, String name, String author, String publisher, int quantity) {  
    this.id = id;  
    this.name = name;  
    this.author = author;  
    this.publisher = publisher;  
    this.quantity = quantity;  
}  
}  
public class applicationofadt{
        public static void main(String[] args) {  
     
   List<Book> list=new ArrayList<Book>();
     Book b1=new Book(101,"Let us C","Yashwant Kanetkar","BPB",8);  
    Book b2=new Book(102,"Data Communications and Networking","Forouzan","Mc Graw Hill",4);  
    Book b3=new Book(103,"Operating System","Galvin","Wiley",6);                                   
                                     
      
   list.add(b1);list.add(b2);list.add(b3);  
   for(Book b:list){  
    System.out.println(b.id+" "+b.name+" "+b.author+" "+b.publisher+" "+b.quantity);  
    } 
   Queue q = new Queue();

   q.deQueue();

    
  q.enQueue(1);
  q.enQueue(2);
  q.enQueue(3);
  q.enQueue(4);
  q.enQueue(5);

    
  q.enQueue(6);

  q.display();

    
   q.deQueue();

    
   q.display();
    Stack s = new Stack(); 
        s.push(10); 
        s.push(20); 
        s.push(30); 
        System.out.println(s.pop() + " Popped from stack"); 
    } 
} 

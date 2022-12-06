# stack-using-arraypublic class stackusingarray {
    private int arr[];
   private int top;
  private  int size=5;
    stackusingarray(){
        size=1;
       arr=new int[size];
       top=-1;
    }
    public   boolean isEmpty(){
       return top==-1;
    }
    public   int isfull(){
        if(top==size-1){
            System.out.println("full");
        }
        return 0;
    }
    public int  push(int x){
        if(top>=size-1)
            resize();
            
        
       return arr[++top]=x;
    }
    public int  pop(){
        if(isEmpty()){
        System.out.println("stack is empty");


        }
        return arr[top--];
        
    }
    public void resize(){
        int []temp=arr;
        size=size*2;
        arr=new int[size];
        for(int i=0;i<=top;i++){
            arr[i]=temp[i];
        }
    }
    public int peek(){
        return arr[top];
    }
    public static  void main(String args[]){
 stackusingarray s=new stackusingarray();
 s.push(34);
 s.push(30);
 s.push(38);
 s.push(39);
 s.push(34);
 s.push(30);
 s.push(38);
 s.push(39);
 System.out.println(s.isEmpty());
 System.out.println(s.isfull());
 System.out.println(s.pop());
 System.out.println(s.peek());


    }
}

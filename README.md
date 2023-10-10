Die bob;
Die rob;
 void setup()
  {
    background((int)(Math.random()*255), (int)(Math.random()*255), (int)(Math.random()*255));
    size(500, 500);  
    noLoop();
  }
  void draw()
  {
      int i = -46;
      int p = -47;
      int j = 449;
      int k = -102;
      while(p < 490){
        bob = new Die(i, p);
        bob.roll();
        bob.show();
        rob = new Die(j, k);
        rob.roll();
        rob.show();
        i = i + 55;
        p = p + 55;
        j = j - 55;
        k = k + 55;
      }
      
  }
  void mousePressed()
  {
      redraw();
  }
  class Die //models one single dice cube
  {
    Die bob; 
    int myX, myY, result;
      
      Die(int x, int y) //constructor
      {
          myX = x;
          myY = y;
          result = 1;
          
      }
      void roll()
      {
        int a = (int)(Math.random()*6);
        result = a + 1;
      }
      void show()
      {
        fill(255);
        rect(myX + 50, myY+ 50, 50, 50);
        
        if (result == 1){
           fill(0);
          ellipse(myX + 75, myY+ 75, 8, 8); 
        }
          else if(result == 2){
           fill(0);
           ellipse(myX + 62, myY+ 62, 8, 8);
           ellipse(myX + 88, myY+ 88, 8, 8);
         
          }
          else if(result == 3){
           fill(0);
           ellipse(myX + 88, myY+ 62, 8, 8);
           ellipse(myX + 75, myY+ 75, 8, 8);
           ellipse(myX + 62, myY+ 88, 8, 8);
          }
          else if(result == 4){
            fill(0);
           ellipse(myX + 62, myY+ 62, 8, 8);
           ellipse(myX + 62, myY+ 88, 8, 8);
           ellipse(myX + 88, myY+ 62, 8, 8);
           ellipse(myX + 88, myY+ 88, 8, 8);
        }
        else if(result == 5){
         fill(0);
           ellipse(myX + 88, myY+ 62, 8, 8);
           ellipse(myX + 75, myY+ 75, 8, 8);
           ellipse(myX + 62, myY+ 88, 8, 8);
           ellipse(myX + 62, myY+ 62, 8, 8);
           ellipse(myX + 88, myY+ 88, 8, 8);
        }
        else if(result == 6){
         fill(0);
         ellipse(myX + 62, myY+ 62, 8, 8);
         ellipse(myX + 75, myY+ 62, 8, 8);
         ellipse(myX + 88, myY+ 62, 8, 8);
         ellipse(myX + 62, myY+ 88, 8, 8);
         ellipse(myX + 75, myY+ 88, 8, 8);
         ellipse(myX + 88, myY+ 88, 8, 8);
         
        }
         
        }
          
      }
   




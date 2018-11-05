
#define ir1 digitalRead(2)
#define ir2 digitalRead(3)
#define ir3 digitalRead(4)
#define ir4 digitalRead(11)
#define ir5 digitalRead(12)
#define ir6 digitalRead(13)


int inr1=5; //pwm
int inr2=7;
int inl1=6; //pwm
int inl2=8;




void setup() {
pinMode(ir1,INPUT);
pinMode(ir2,INPUT);
pinMode(ir3,INPUT);
pinMode(ir4,INPUT);
pinMode(ir5,INPUT);
pinMode(ir6,INPUT);

  
pinMode(inr1,OUTPUT);
pinMode(inr2,OUTPUT);
pinMode(inl1,OUTPUT);
pinMode(inl2,OUTPUT);


  }


void loop()
{
    
      if(!ir1 && !ir2 && ( ir3 || ir4 ) && !ir5 && !ir6 )
      {
          motor_foward();
      }
      else if( ( ir1 || ir2 || ir3 ) && !ir4 && !ir5 && !ir6 )
      {
         motor_left();
      }
          
      else if(!ir1 && !ir2 && !ir3 && ( ir4 || ir5 || ir6 ) )
      {
         motor_right();
      }
              

              

     /*motor_foward();
     delay(1000);
     motor_backward();
     delay(1000);
     motor_left();
     delay(1000);
     motor_right();
     delay(1000);*/
  
  

}


  void motor_foward()
  {
      analogWrite(inr1,255-80);
      digitalWrite(inr2,HIGH);
      analogWrite(inl1,255-80);
      digitalWrite(inl2,HIGH);
      
  }
  void motor_backward()
  {
      analogWrite(inr1,80);
      digitalWrite(inr2,LOW);
      analogWrite(inl1,80);
      digitalWrite(inl2,LOW);
  }
  
  void motor_left()
  {
      analogWrite(inr1,255-80);
      digitalWrite(inr2,HIGH);
      analogWrite(inl1,0);
      digitalWrite(inl2,HIGH);
  }
    
  void motor_right()
  {
      analogWrite(inr1,0);
      digitalWrite(inr2,HIGH);
      analogWrite(inl1,255-80);
      digitalWrite(inl2,HIGH);
  }



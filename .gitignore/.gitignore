#include <QTRSensors.h>
#define NUM_SENSORS  6
#define EMITTER_PIN 8

#define PWMa 10
#define a1 7
#define a2 8

#define PWMb 9
#define b1 6
#define b2 5


QTRSensorsAnalog qtrrc((unsigned char[]) {  A0, A1, A2, A3, A4, A5 } , NUM_SENSORS, EMITTER_PIN);
unsigned int sensorValues[NUM_SENSORS];

void setup()
{
  Serial.begin(9600);
  
  pinMode(a1, OUTPUT);
  pinMode(a2, OUTPUT);
  pinMode(PWMa, OUTPUT);
  pinMode(b1, OUTPUT);
  pinMode(b2, OUTPUT);
  pinMode(PWMb, OUTPUT);
  

  int i;
  for (int i = 0; i < 250; i++)
  {
    qtrrc.calibrate();
    delay(10);  
  }
    delay(1000);
  }

void loop()
{
  unsigned int sensors[6];
  int position = qtrrc.readLine(sensors);
  Serial.println(position);

  if(position<=500)
    {
   digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,100);                                                                                                                                           
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,0);
    }
  else  if(position<=1000)
    {
   digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,120);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,20);
    }
    else if(position<=1500)
     {
   digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,140);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,40);
    
    }
      else if(position<=2000)
   {
     digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,160);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,60);
    }
     else if(position>=2500 && position<=3000)
     {
  digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,200);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,200);
   }
    else if(position<=3500)
  {
  digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,60);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,160);
    
  }
  else  if(position<=4000)
  { 
  digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,40);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,140);
  }

else if(position<=4500)

  { 
  digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,20);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,120);
  
  }

else if(position<=5000 )

  { 
  digitalWrite(a1, HIGH);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,0);
  digitalWrite(b1, HIGH);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,100);
  
  }
  else
  {
    digitalWrite(a1, LOW);
  digitalWrite(a2, LOW);
  analogWrite(PWMa,0);
  digitalWrite(b1, LOW);
  digitalWrite(b2, LOW);
  analogWrite(PWMb,0);
  }
  
}

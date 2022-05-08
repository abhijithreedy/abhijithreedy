//Alcohol Detector
const int MQ3=0;
const int LED=9;
int value;

void setup() {
  Serial.begin(9600);
  pinMode(MQ3, INPUT);
  pinMode(LED, OUTPUT);//if you want you can put buzzer in place led or both in the programme
  digitalWrite(LED,LOW);

}

void loop()
{
  value= analogRead(MQ3);
  Serial.println(value);
  
  if(value>500)
  {
    digitalWrite(LED,HIGH);
  }
  else
  {
    digitalWrite(LED,LOW);
  }

  delay (500);
}

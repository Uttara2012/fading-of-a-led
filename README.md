# fading-of-a-led
int led = 3;
int brightness = 0;    // how bright the LED is
int fadeAmount = 5;    // how many points to fade the LED by

// the setup routine runs once when you press reset:
void setup()  { 
 
  pinMode(led, OUTPUT);
} 


void loop()  { 
  
  analogWrite(led, brightness);    

 
  brightness = brightness + fadeAmount;

  
  if (brightness == 0 || brightness == 255) {
    fadeAmount = -fadeAmount ; 
  }     
  
  delay(30);                            
}

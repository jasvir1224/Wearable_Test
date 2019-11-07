#include <InternetButton.h>

InternetButton button = InternetButton();


int counter = 0;
int seconds = 20; 

void setup() {

button.begin();
}
void loop() {
    if(button.buttonOn(1)){
     button.allLedsOn(255,0,0);
      delay(400);
     button.allLedsOff();
    counter = counter + 1;
 if((counter % 60 == 0) && (seconds > 0)){
        seconds = seconds - 1;
        for(int i = 0; i >= 6 ; i ++){
                     button.ledOn(i,255,255,255); 
                     delay(200);
                     }
    }
  


}
    
}

    

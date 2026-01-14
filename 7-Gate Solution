const int btnA = 2;
const int btnB = 3;
const int btnC = 4;
const int btnD = 5;
const int ledPin = 13;

void setup() {
  pinMode(btnA, INPUT_PULLUP); //
  pinMode(btnB, INPUT_PULLUP);
  pinMode(btnC, INPUT_PULLUP);
  pinMode(btnD, INPUT_PULLUP);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  bool sbtnA = !digitalRead(btnA); //INPUT_PULLUP makes it so that LOW means pressed, so a not is done so that HIGH means pressed, which now means 1, now able to be used in the Boolean Algebra :D
  bool sbtnB = !digitalRead(btnB);
  bool sbtnC = !digitalRead(btnC);
  bool sbtnD = !digitalRead(btnD);

  delay(20);

//Logical Operations from the wonderful 7-Gate Solution, my friend had provided  
//This will turn on 0, 1, 2, 3, 4, 5, 10, 11, 12, 13, 15
//This will turn off 6, 7, 8, 9, 14
//The Nots were groups, and then placed a not over all of it
  bool AD = (sbtnA && sbtnD);
  bool nBC = !(sbtnB && sbtnC);
  bool oabove = (AD || nBC);

  bool nD = !(sbtnD);
  bool onDC = (sbtnC || nD);
  bool oonDCB = (sbtnB || onDC);

  //Final gate operation
  bool finalResult = (oonDCB && oabove);
//7-Gates :D
  delay(20);
  
  digitalWrite(ledPin, finalResult);
  delay(20);
}
//#Khetarpal Solution PHS
//January 13th, 2026

void setup() {
  Serial.begin(9600);
  pinMode(A0,INPUT);
  pinMode(A1,INPUT);
}

void loop() {

  int sensor1_data = analogRead(sensor1);
  int sensor2_data = analogRead(sensor2);
  long timestamp = millis();
  
  String dataline = String(sensor1_data) + "," + String(sensor2_data) + "," + timestamp + ";";
  Serial.print(dataline);
  delay(70); 
}

## 3 Potenciometros controlan el color de un led RGB

Cambiando los valores de los potenciometros se pueden conseguir diferentes colores en un Led RGB

# Codigo de Arduino

int rojo = 6;
int intensidadRojo;
int verde = 5;
int intensidadVerde;
int azul = 3;
int intensidadAzul;
int potRojo = A0;
int valPotRojo;
int potVerde = A1;
int valPotVerde;
int potAzul = A2;
int valPotAzul;

void setup()
{
    pinMode(rojo, OUTPUT);
    pinMode(verde, OUTPUT);
    pinMode(azul, OUTPUT);
}

void loop()
{
    valPotRojo = analogRead(potRojo);
    intensidadRojo = map (valPotRojo, 0, 1023, 0, 255);
    analogWrite(rojo, intensidadRojo);
    valPotVerde = analogRead(potVerde);
    intensidadVerde = map (valPotVerde, 0, 1023, 0, 255);
    analogWrite(verde, intensidadVerde);
    valPotAzul = analogRead(potAzul);
    intensidadAzul = map (valPotAzul, 0, 1023, 0, 255);
    analogWrite(azul, intensidadAzul);
}

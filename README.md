//Perfil-Githun-y-Gitlab
//Conexion de pantalla tft 9341 al microcontrolador esp 32

//Añadir librerias y driver para controlar la pantalla tft
#include <Adafruit_GFX.h>
#include <Adafruit_ILI9341.h>

// Definir los pines del ESP32
#define TFT_CS   5
#define TFT_RST  4
#define TFT_RS   2
#define TFT_SCLK 18
#define TFT_MOSI 23

// Crear un objeto de la pantalla TFT
Adafruit_ILI9341 tft = Adafruit_ILI9341(TFT_CS, TFT_RS, TFT_RST);

void setup() {
  Serial.begin(115200);
  tft.begin();
  tft.setRotation(3);  // Ajustar la orientación según sea necesario
  tft.fillScreen(ILI9341_BLACK); // Limpia la pantalla con color negro
  
  // Dibujar un rectángulo rojo
  tft.fillRect(50, 50, 100, 100, ILI9341_RED);
}

void loop() {
}

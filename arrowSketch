
#include <FastLED.h>

#define LED_PIN    3
#define NUM_LEDS    23
#define BRIGHTNESS  100
#define LED_TYPE    WS2811
#define COLOR_ORDER GRB
CRGB leds[NUM_LEDS];

uint8_t colorPick;

// Custom color array
CRGB colorArray[] = {
  CRGB::Red,
  CRGB::Blue,
  CRGB::DarkCyan,
  CRGB::SlateBlue,
  CRGB::DarkMagenta,
  CRGB::Indigo,
  CRGB::MediumVioletRed,
  CRGB::Sienna,
  CRGB::DarkGreen,
  CRGB::DarkOrange,
};

void setup() {
    delay( 3000 ); // power-up safety delay
    FastLED.addLeds<LED_TYPE, LED_PIN, COLOR_ORDER>(leds, NUM_LEDS).setCorrection( TypicalLEDStrip );
    FastLED.setBrightness(  BRIGHTNESS );
}


void loop() {
  //pick a random color from the custom color array
  colorPick = random8( sizeof(colorArray) / sizeof(colorArray[0]) );

  for (uint8_t i = 0; i < NUM_LEDS; i++) {
    if (i < 11) {
      leds[i] = colorArray[colorPick];   
    }
    if (i == 11) {
        leds[i] = colorArray[colorPick];
        leds[i+7] = colorArray[colorPick];
        leds[i+11]  = colorArray[colorPick];
    }
    if (i == 12) {
        leds[i] = colorArray[colorPick];
        leds[i+5] = colorArray[colorPick];
        leds[i+9]  = colorArray[colorPick];
    }
    if (i == 13) {
      leds[i] = colorArray[colorPick];
      leds[i+3] = colorArray[colorPick];
      leds[i+7]  = colorArray[colorPick];
    }
    if (i == 14) {
      leds[i] = colorArray[colorPick];
      leds[i+1] = colorArray[colorPick];
      leds[i+5]  = colorArray[colorPick];      
    }
    //leds[i] = colorArray[colorPick];
    FastLED.show();
    delay(150);
    //fadeToBlackBy(leds, NUM_LEDS, 220);
    fadeToBlackBy(leds, NUM_LEDS, 75);

  }
  
}


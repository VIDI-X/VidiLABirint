# VidiLABirint

R201 – add 

```C++ 
      } else if (world[y][x] == key) { 
        tft.fillRect(x * ssf, y * ssf, CELL, CELL, ILI9341_GREEN); 
            
``` 


R241 – add 

```C++ 
      if (world[y][x] == key && world[y - 1][x] == Player) { 
        world[y][x] = Player; 
        world[y - 1][x] = empty; 
        PlayerKeys++; 
        Serial.print("PlayerKeys: "); 
        Serial.println(PlayerKeys); 
      } 

``` 

 
R58 – replace 

```C++ 
                          1, 1, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1,

``` 
 

R32 – add 

```C++ 
int PlayerKeys = 0;// Koliko ključeva na raspolaganju ima igrač 

``` 
 

R260 – add 

```C++ 
      if (world[y][x] == key && world[y + 1][x] == Player) { 
        world[y][x] = Player; 
        world[y + 1][x] = empty; 
        PlayerKeys++; 
        Serial.print("PlayerKeys: "); 
        Serial.println(PlayerKeys); 
      } 

``` 
 

R278 – add 

```C++ 
      if (world[y][x] == key && world[y][x + 1] == Player) { 
        world[y][x] = Player; 
        world[y][x + 1] = empty; 
        PlayerKeys++; 
        Serial.print("PlayerKeys: "); 
        Serial.println(PlayerKeys); 
      } 

``` 
 

R296 – add 

```C++ 
      if (world[y][x] == key && world[y][x - 1] == Player) { 
        world[y][x] = Player; 
        world[y][x - 1] = empty; 
        PlayerKeys++; 
        Serial.print("PlayerKeys: "); 
        Serial.println(PlayerKeys); 
      } 

``` 
 

R58 – R59 – replace 

```C++ 
                           1, 1, 1, 0, 2, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 
                           1, 1, 1, 2, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 
``` 
 

R33 – add 

```C++ 
#define ILI9341_NAVYBLUE 0x006E //https://www.barth-dev.de/online/rgb565-color-picker/ 

``` 


R206 – add 

```C++ 
      } else if (world[y][x] == door) { 
        tft.fillRect(x * ssf, y * ssf, CELL, CELL, ILI9341_NAVYBLUE); 

``` 

 
R308 – add 

```C++ 
      if (world[y][x] == door && world[y][x - 1] == Player && PlayerKeys > 0 ) { 
        world[y][x] = Player; 
        world[y][x - 1] = empty; 
        PlayerKeys--; 
        Serial.print("PlayerKeys: "); 
        Serial.println(PlayerKeys); 
      } 

``` 
 

R59 – R62 – replace 

```C++ 
                           1, 1, 1, 0, 0, 0, 9, 0, 1, 0, 0, 0, 0, 0, 4, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 
                           1, 1, 1, 0, 2, 2, 0, 0, 3, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 
                           1, 1, 1, 2, 2, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 
                           1, 1, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 5, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 0, 0, 0, 1, 1, 1, 1, 1, 
``` 

R208 – add 

```C++ 
      } else if (world[y][x] == vampire) { 
        tft.fillRect(x * ssf, y * ssf, CELL, CELL, ILI9341_CYAN); 
      } else if (world[y][x] == garlic) { 
        tft.fillRect(x * ssf, y * ssf, CELL, CELL, ILI9341_YELLOW); 

``` 
 

R319 – add 

```C++ 
      if (world[y][x] == vampire && world[y][x - 1] == Player && PlayerGarlic > 0 ) { 
        world[y][x] = Player; 
        world[y][x - 1] = empty; 
        PlayerGarlic--; 
        Serial.print("PlayerGarlic: "); 
        Serial.println(PlayerGarlic); 
      } 
      if (world[y][x] == vampire && world[y][x - 1] == Player && PlayerGarlic < 1 ) { 
        YouDied(); 
      } 

``` 

R298 – add 

```C++ 
void YouDied() { 
  for (int n = 0; n < 9; n++) { 
    generateRandomPattern(); 
    drawWorld(); 
    delay(speed * n); 
  } 
  fill_world_edges(); 
  drawWorld(); 
  loadWorld(); 
} 

``` 

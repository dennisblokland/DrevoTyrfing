# DrevoTyrfing
Protocol Discription of the Drevo Tyrfing V2

Vendor: 0x0416 
Device: 0xA0F8

This discription is far from complete.
## Message

**Color message**
#a color packet looks like this:

06 be 19 00 01 01 0e 29 2c 4b 4e 4d ff 45 45 00 ff 00 ff 00 ff 00 ff 08 ff 00 ff 00 ff 00 ff ff

|byte        |  Description  | example                                        |
|------------|---------------|----------------------------------------------|
|     0-6    |  Mode settings| 06 be 19 00 01 01 0e is custom color mode    |
|     7-11   |    Keys       | key identifiers                             |
|     12     | spacer        | 0                                            |
|     13-15  |  RGB key 1    |                                              |
|     16     |spacer         | 0                                            |
|     17-19  |   RGB key 2   |                                              |
|     20     |   spacer      | 0                                            |
|     21-23  |   RGB key 3   |                                              |
|     24     |    spacer     | 0                                            |
|     25-27  |  RGB key 4    |                                              |
|     28     |  spacer       |                                              |
|     29-31  |  RGB key 5    |                                              |

## Key identifiers

  the identifiers are based on the hid scan codes found here:
  https://gist.github.com/MightyPork/6da26e382a7ad91b5496ee55fdc73db2
  
  this is a grid is made of the keyboard
```
esc       f1        f2        f3          f4          f5        f6        f7        f8        f9       f10        f11       f12       f13     PS        SL      PB
0x29,    0x3a,     0x3b,     0x3c,       0x3d,       0x00,      0x3e,     0x3f,     0x40,    0x41,    0x42,      0x43,      0x44,     0x45,   0x46,    0x47 ,   

~         1         2         3           4           5           6       7           8       9         0         -           =       BACKS    ins      home    p-up
0x35,    0x1e,     0x1f,     0x20,       0x21,       0x22,      0x23,     0x24,     0x25,    0x26,    0x27,      0x2d,      0x2e,     0x2a,   0x49,    0x4a,    0x4b

tab       q         w         e           r            t         y         u         i         o       p           [          ]         \      del      end     p-down
0x2b,    0x14,     0x1a,     0x08,       0x15,       0x17,      0x1c,     0x18,     0x0c,    0x12,    0x13,      0x2f,      0x30,     0x31,   0x4c,    0x4d,    0x4e

caps      a         s          d          f           g           h         j         k       l          ;        '         enter               
0x39,    0x04,     0x16,     0x07,       0x09,       0x0a,      0x0b,     0x0d,     0x0e,    0x0f,    0x33,      0x34,      0x28,     

shift     z         x         c           v           b           n         m         ,       .         /        shift                                   up                     
0xe1,    0x1d,     0x1b,     0x06,       0x19,       0x05,      0x11,     0x10,     0x36,    0x37,    0x38,      0xe5,      0x00,     0x00,   0x00,    0x52,    0x00

ctrl      win        alt                                        space                                   alt        FN       compo     ctrl    left     down    right
0xe0,    0xe3 ,    0xe2 ,    0x00,       0x00,       0x00,      0x2c,     0x00,     0x00,    0x00,    0xe6,      0xed,      0x65,     0xe4,   0x50,    0x51,    0x4f
```

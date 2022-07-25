---
UID: NE:icm.__unnamed_enum_4
title: BMFORMAT
description: The values of the **BMFORMAT** enumerated type are used by several WCS functions to indicate the format that particular bitmaps are in.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - BMFORMAT
f1_keywords:
 - BMFORMAT
 - icm/BMFORMAT
dev_langs:
 - c++
---

## -description

The values of the **BMFORMAT** enumerated type are used by several WCS functions to indicate the format that particular bitmaps are in.

## -enum-fields

### -field BM_x555RGB:0x0000

16 bits per pixel. RGB color space. 5 bits per channel. The most significant bit is ignored.

### -field BM_x555XYZ:0x0101

16 bits per pixel. CIE device-independent XYZ color space. 5 bits per channel. The most significant bit is ignored.

### -field BM_x555Yxy

16 bits per pixel. Yxy color space. 5 bits per channel. The most significant bit is ignored.

### -field BM_x555Lab

16 bits per pixel. L\*a\*b color space. 5 bits per channel. The most significant bit is ignored.

### -field BM_x555G3CH

16 bits per pixel. G3CH color space. 5 bits per channel. The most significant bit is ignored.

### -field BM_RGBTRIPLETS:0x0002

24 bits per pixel maximum. For three channel colors, such as Red,Green,Blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.

### -field BM_BGRTRIPLETS:0x0004

24 bits per pixel maximum. For three channel colors, such as Red,Green,Blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.

### -field BM_XYZTRIPLETS:0x0201

24 bits per pixel maximum. For three channel, X, Y and Z values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

> [!Note]  
> The [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) function does not support [**BM\_XYZTRIPLETS**](/windows/win32/api/icm/ne-icm-bmformat) as an input.

### -field BM_YxyTRIPLETS

24 bits per pixel maximum. For three channel, Y, x and y values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

> [!Note]  
> The [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) function does not support [**BM\_YxyTRIPLETS**](/windows/win32/api/icm/ne-icm-bmformat) as an input.

### -field BM_LabTRIPLETS

24 bits per pixel maximum. For three channel, L, a and b values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

### -field BM_G3CHTRIPLETS

24 bits per pixel maximum. For three channel values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

### -field BM_5CHANNEL

40 bits per pixel. 8 bits apiece are used for each channel.

### -field BM_6CHANNEL

48 bits per pixel. 8 bits apiece are used for each channel.

### -field BM_7CHANNEL

56 bits per pixel. 8 bits apiece are used for each channel.

### -field BM_8CHANNEL

64 bits per pixel. 8 bits apiece are used for each channel.

### -field BM_GRAY

32 bits per pixel. Only the 8 bit gray-scale value is used.

### -field BM_xRGBQUADS:0x0008

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.

### -field BM_xBGRQUADS:0x0010

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.

### -field BM_xG3CHQUADS:0x0304

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.

### -field BM_KYMCQUADS

32 bits per pixel. 8 bits are used for each color channel.

### -field BM_CMYKQUADS:0x0020

32 bits per pixel. 8 bits are used for each color channel.

### -field BM_10b_RGB:0x0009

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.

### -field BM_10b_XYZ:0x0401

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.

### -field BM_10b_Yxy

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.

### -field BM_10b_Lab

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.

### -field BM_10b_G3CH

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.

### -field BM_NAMED_INDEX

32 bits per pixel. Named color indices. Index numbering begins at 1.

### -field BM_16b_RGB:0x000A

48 bits per pixel. Each channel uses 16 bits.

### -field BM_16b_XYZ:0x0501

48 bits per pixel. Each channel uses 16 bits.

### -field BM_16b_Yxy

48 bits per pixel. Each channel uses 16 bits.

### -field BM_16b_Lab

48 bits per pixel. Each channel uses 16 bits.

### -field BM_16b_G3CH

48 bits per pixel. Each channel uses 16 bits.

### -field BM_16b_GRAY

16 bits per pixel.

### -field BM_565RGB:0x0001

16 bits per pixel. 5 bits are used for red, 6 for green, and 5 for blue.

### -field BM_32b_scRGB:0x0601

96 bits per pixel, 32 bit per channel IEEE floating point.

### -field BM_32b_scARGB:0x0602

128 bits per pixel, 32 bit per channel IEEE floating point.

### -field BM_S2DOT13FIXED_scRGB:0x0603

48 bits per pixel, Fixed point integer ranging from -4 to +4 with a sign bit and 2 bit exponent and 13 bit mantissa.

### -field BM_S2DOT13FIXED_scARGB:0x0604

64 bits per pixel, Fixed point integer ranging from -4 to +4 with a sign bit and 2 bit exponent and 13 bit mantissa.

### -field BM_R10G10B10A2:0x0701

32 bits per pixel. 10 bits are used for each color channel. The two most significant bits are alpha.

### -field BM_R10G10B10A2_XR:0x0702

32 bits per pixel. 10 bits are used for each color channel. The 10 bits of each color channel are 2.8 fixed point with a -0.75 bias, giving a range of \[-0.76 .. 1.25\]. This range corresponds to \[-0.5 .. 1.5\] in a gamma = 1 space. The two most significant bits are preserved for alpha.

This uses an extended range (XR) sRGB color space. It has the same RGB primaries, white point, and gamma as sRGB.

### -field BM_R16G16B16A16_FLOAT:0x0703

64 bits per pixel. Each channel is a 16-bit float. The last WORD is alpha.

## -remarks

### Table of bitmap formats

The follow table shows, for each of the formats, the number of bits per pixel, the number of channels, the order of the channels, and the bit-by-bit structure of each byte. You might have to scroll to the right to see all the columns of the table.

| Format                   | Bits Per Pixel | Number of Channels | Channel Ordering | Byte 0                   | Byte 1                         | Byte 2                   | Byte 3                         | Byte 4                   | Byte 5                         | Byte 6                   | Byte 7                   |
|--------------------------|----------------|--------------------|------------------|--------------------------|--------------------------------|--------------------------|--------------------------------|--------------------------|--------------------------------|--------------------------|--------------------------|
| BM\_GRAY                 | 8              | 1                  |                  | K7K6K5K4K3K2K1K0         |                                |                          |                                |                          |                                |                          |                          |
| BM\_565RGB               | 16             | 3                  | BGR              | G2G1G0B4B3B2B1B0         | R4R3R2R1R0G5G4G3               |                          |                                |                          |                                |                          |                          |
| BM\_x555RGB              | 16             | 3                  | BGR              | G2G1G0B4B3B2B1B0         | xR4R3R2R1R0G4G3                |                          |                                |                          |                                |                          |                          |
| BM\_x555XYZ              | 16             | 3                  | ZYX              | Y2Y1Y0Z4Z3Z2Z1Z0         | xX4X3X2X1X0Y4Y3                |                          |                                |                          |                                |                          |                          |
| BM\_x555Yxy              | 16             | 3                  | yxY              | x2x1x0y4y3y2y1y0         | xY4Y3Y2Y1Y0x4x3                |                          |                                |                          |                                |                          |                          |
| BM\_x555Lab              | 16             | 3                  | baL              | a2a1a0b4b3b2b1b0         | xL4L3L2L1L0a4a3                |                          |                                |                          |                                |                          |                          |
| BM\_x555G3CH             | 16             | 3                  | 123              | xC14C13C12C11C10C24C23   | C22C21C20C34C33C32C31C30       |                          |                                |                          |                                |                          |                          |
| BM\_16b\_GRAY            | 16             | 1                  | K                | K7K6K5K4K3K2K1K0         | K15K14K13K12K11K10K9K8         |                          |                                |                          |                                |                          |                          |
| BM\_RGBTRIPLETS          | 24             | 3                  | BGR              | B7B6B5B4B3B2B1B0         | G7G6G5G4G3G2G1G0               | R7R6R5R4R3R2R1R0         |                                |                          |                                |                          |                          |
| BM\_BGRTRIPLETS          | 24             | 3                  | RGB              | R7R6R5R4R3R2R1R0         | G7G6G5G4G3G2G1G0               | B7B6B5B4B3B2B1B0         |                                |                          |                                |                          |                          |
| BM\_XYZTRIPLETS          | 24             | 3                  | XYZ              | X7X6X5X4X3X2X1X0         | Y7Y6Y5Y4Y3Y2Y1Y0               | Z7Z6Z5Z4Z3Z2Z1Z0         |                                |                          |                                |                          |                          |
| BM\_YxyTRIPLETS          | 24             | 3                  | Yxy              | Y7Y6Y5Y4Y3Y2Y1Y0         | x7x6x5x4x3x2x1x0               | y7y6y5y4y3y2y1y0         |                                |                          |                                |                          |                          |
| BM\_LabTRIPLETS          | 24             | 3                  | Lab              | L7L6L5L4L3L2L1L0         | a7a6a5a4a3a2a1a0               | b7b6b5b4b3b2b1b0         |                                |                          |                                |                          |                          |
| BM\_G3CHTRIPLETS         | 24             | 3                  | 123              | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 |                                |                          |                                |                          |                          |
| BM\_xRGBQUADS            | 32             | 3                  | BGRx             | B7B6B5B4B3B2B1B0         | G7G6G5G4G3G2G1G0               | R7R6R5R4R3R2R1R0         | xxxxxxxx                       |                          |                                |                          |                          |
| BM\_xBGRQUADS            | 32             | 3                  | RGBx             | R7R6R5R4R3R2R1R0         | G7G6G5G4G3G2G1G0               | B7B6B5B4B3B2B1B0         | xxxxxxxx                       |                          |                                |                          |                          |
| BM\_xG3CHQUADS           | 32             | 3                  | 123x             | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 | xxxxxxxx                       |                          |                                |                          |                          |
| BM\_CMYKQUADS            | 32             | 4                  | KYMC             | K7K6K5K4K3K2K1K0         | Y7Y6Y5Y4Y3Y2Y1Y0               | M7M6M5M4M3M2M1M0         | C7C6C5C4C3C2C1C0               |                          |                                |                          |                          |
| BM\_KYMCQUADS            | 32             | 4                  | CMYK             | C7C6C5C4C3C2C1C0         | M7M6M5M4M3M2M1M0               | Y7Y6Y5Y4Y3Y2Y1Y0         | K7K6K5K4K3K2K1K0               |                          |                                |                          |                          |
| BM\_10b\_RGB             | 32             | 3                  | BGR              | B7B6B5B4B3B2B1B0         | G5G4G3G2G1G0B9B8               | R3R2R1R0G9G8G7G6         | xxR9R8R7R6R5R4                 |                          |                                |                          |                          |
| BM\_10b\_XYZ             | 32             | 3                  | ZYX              | Z7Z6Z5Z4Z3Z2Z1Z0         | Y5Y4Y3Y2Y1Y0Z9Z8               | X3X2X1X0Y9Y8Y7Y6         | xxX9X8X7X6X5X4                 |                          |                                |                          |                          |
| BM\_10b\_Yxy             | 32             | 3                  | yxY              | y7y6y5y4y3y2y1y0         | x5x4x3x2x1x0y9y8               | Y3Y2Y1Y0x9x8x7x6         | xxY9Y8Y7Y6Y5Y4                 |                          |                                |                          |                          |
| BM\_10b\_Lab             | 32             | 3                  | baL              | b7b6b5b4b3b2b1b0         | a5a4a3a2a1a0b9b8               | L3L2L1L0a9a8a7a6         | xxL9L8L7L6L5L4                 |                          |                                |                          |                          |
| BM\_10b\_G3CH            | 32             | 3                  | 321              | C37C36C35C34C33C32C31C30 | C25C24C23C22C21C20C39C38       | C13C12C11C10C29C28C27C26 | xxC19C18C17C16C15C14           |                          |                                |                          |                          |
| BM\_NAMED\_INDEX         | 32             |                    |                  | n7n6n5n4n3n2n1n0         | n15n14n13n12n11n10n9n8         | n23n22n21n20n19n18n17n16 | n31n30n29n28n27n26n25n24       |                          |                                |                          |                          |
| BM\_5CHANNEL             | 40             | 5                  | 12345            | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 | C47C46C45C44C43C42C41C40       | C57C56C55C54C53C52C51C50 |                                |                          |                          |
| BM\_6CHANNEL             | 48             | 6                  | 123456           | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 | C47C46C45C44C43C42C41C40       | C57C56C55C54C53C52C51C50 | C67C66C65C64C63C62C61C60       |                          |                          |
| BM\_16b\_RGB             | 48             | 3                  | RGB              | R7R6R5R4R3R2R1R0         | R15R14R13R12R11R10R9R8         | G7G6G5G4G3G2G1G0         | G15G14G13G12G11G10G9G8         | B7B6B5B4B3B2B1B0         | B15B14B13B12B11B10B9B8         |                          |                          |
| BM\_16b\_XYZ             | 48             | 3                  | XYZ              | X7X6X5X4X3X2X1X0         | X15X14X13X12X11X10X9X8         | Y7Y6Y5Y4Y3Y2Y1Y0         | Y15Y14Y13Y12Y11Y10Y9Y8         | Z7Z6Z5Z4Z3Z2Z1Z0         | Z15Z14Z13Z12Z11Z10Z9Z8         |                          |                          |
| BM\_16b\_Lab             | 48             | 3                  | Lab              | L7L6L5L4L3L2L1L0         | L15L14L13L12L11L10L9L8         | a7a6a5a4a3a2a1a0         | a15a14a13a12a11a10a9a8         | b7b6b5b4b3b2b1b0         | b15b14b13b12b11b10b9b8         |                          |                          |
| BM\_16b\_G3CH            | 48             | 3                  | 321              | C37C36C35C34C33C32C31C30 | C315C314C313C312C311C310C39C38 | C27C26C25C24C23C22C21C20 | C215C214C213C212C211C210C29C28 | C17C16C15C14C13C12C11C10 | C115C114C113C112C111C110C19C18 |                          |                          |
| BM\_16b\_Yxy             | 48             | 3                  | Yxy              | Y7Y6Y5Y4Y3Y2Y1Y0         | Y15Y14Y13Y12Y11Y10Y9Y8         | x7x6x5x4x3x2x1x0         | x15x14x13x12x11x10x9x8         | y7y6y5y4y3y2y1y0         | y15y14y13y12y11y10y9y8         |                          |                          |
| BM\_7CHANNEL             | 56             | 7                  | 1234567          | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 | C47C46C45C44C43C42C41C40       | C57C56C55C54C53C52C51C50 | C67C66C65C64C63C62C61C60       | C77C76C75C74C73C72C71C70 |                          |
| BM\_8CHANNEL             | 64             | 8                  | 12345678         | C17C16C15C14C13C12C11C10 | C27C26C25C24C23C22C21C20       | C37C36C35C34C33C32C31C30 | C47C46C45C44C43C42C41C40       | C57C56C55C54C53C52C51C50 | C67C66C65C64C63C62C61C60       | C77C76C75C74C73C72C71C70 | C87C86C85C84C83C82C81C80 |
| BM\_32b\_scRGB           | 96             | 3                  | BGR              |                          |                                |                          |                                |                          |                                |                          |                          |
| BM\_32b\_scARGB          | 128            | 3                  | BGRA             |                          |                                |                          |                                |                          |                                |                          |                          |
| BM\_S2DOT13FIXED\_scRGB  | 48             | 3                  | BGR              |                          |                                |                          |                                |                          |                                |                          |                          |
| BM\_S2DOT13FIXED\_scARGB | 64             | 3                  | BGRA             |                          |                                |                          |                                |                          |                                |                          |                          |
| BM\_R10G10B10A2          | 32             | 3                  | ABGR             | A7A6B5B4B3B2B1B0         | B7B6B5B4G3G2G1G0               | G7G6G5G4G3G2R1R0         | R7R6R5R4R3R2R1R0               |                          |                                |                          |                          |
| BM\_R10G10B10A2\_XR      | 32             | 3                  | ABGR             | A7A6B5B4B3B2B1B0         | B7B6B5B4G3G2G1G0               | G7G6G5G4G3G2R1R0         | R7R6R5R4R3R2R1R0               |                          |                                |                          |                          |
| BM\_R16G16B16A16\_FLOAT  | 64             | 3                  | RGBA             | R7R6R5R4R3R2R1R0         | R7R6R5R4R3R2R1R0               | G7G6G5G4G3G2G1G0         | G7G6G5G4G3G2G1G0               | B7B6B5B4B3B2B1B0         | B7B6B5B4B3B2B1B0               | A7A6A5A4A3A2A1A0         | A7A6A5A4A3A2A1A0         |

## -see-also

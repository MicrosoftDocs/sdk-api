---
UID: NE:icm.BMFORMAT
title: BMFORMAT
author: windows-sdk-content
description: The values of the BMFORMAT enumerated type are used by several WCS functions to indicate the format that particular bitmaps are in.
old-location: wcs\bmformat.htm
tech.root: WCS
ms.assetid: 2388f1b7-af70-4058-a145-abb13159766c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PBMFORMAT, BMFORMAT, BMFORMAT enumeration [Windows Color System], BM_10b_G3CH, BM_10b_Lab, BM_10b_RGB, BM_10b_XYZ, BM_10b_Yxy, BM_16b_G3CH, BM_16b_GRAY, BM_16b_Lab, BM_16b_RGB, BM_16b_XYZ, BM_16b_Yxy, BM_32b_scARGB, BM_32b_scRGB, BM_565RGB, BM_5CHANNEL, BM_6CHANNEL, BM_7CHANNEL, BM_8CHANNEL, BM_BGRTRIPLETS, BM_CMYKQUADS, BM_G3CHTRIPLETS, BM_GRAY, BM_KYMCQUADS, BM_LabTRIPLETS, BM_NAMED_INDEX, BM_R10G10B10A2, BM_R10G10B10A2_XR, BM_R16G16B16A16_FLOAT, BM_RGBTRIPLETS, BM_S2DOT13FIXED_scARGB, BM_S2DOT13FIXED_scRGB, BM_XYZTRIPLETS, BM_YxyTRIPLETS, BM_x555G3CH, BM_x555Lab, BM_x555RGB, BM_x555XYZ, BM_x555Yxy, BM_xBGRQUADS, BM_xG3CHQUADS, BM_xRGBQUADS, LPBMFORMAT, LPBMFORMAT enumeration pointer [Windows Color System], PBMFORMAT, PBMFORMAT enumeration pointer [Windows Color System], _color_BMFORMAT, icm/BMFORMAT, icm/BM_10b_G3CH, icm/BM_10b_Lab, icm/BM_10b_RGB, icm/BM_10b_XYZ, icm/BM_10b_Yxy, icm/BM_16b_G3CH, icm/BM_16b_GRAY, icm/BM_16b_Lab, icm/BM_16b_RGB, icm/BM_16b_XYZ, icm/BM_16b_Yxy, icm/BM_32b_scARGB, icm/BM_32b_scRGB, icm/BM_565RGB, icm/BM_5CHANNEL, icm/BM_6CHANNEL, icm/BM_7CHANNEL, icm/BM_8CHANNEL, icm/BM_BGRTRIPLETS, icm/BM_CMYKQUADS, icm/BM_G3CHTRIPLETS, icm/BM_GRAY, icm/BM_KYMCQUADS, icm/BM_LabTRIPLETS, icm/BM_NAMED_INDEX, icm/BM_R10G10B10A2, icm/BM_R10G10B10A2_XR, icm/BM_R16G16B16A16_FLOAT, icm/BM_RGBTRIPLETS, icm/BM_S2DOT13FIXED_scARGB, icm/BM_S2DOT13FIXED_scRGB, icm/BM_XYZTRIPLETS, icm/BM_YxyTRIPLETS, icm/BM_x555G3CH, icm/BM_x555Lab, icm/BM_x555RGB, icm/BM_x555XYZ, icm/BM_x555Yxy, icm/BM_xBGRQUADS, icm/BM_xG3CHQUADS, icm/BM_xRGBQUADS, icm/LPBMFORMAT, icm/PBMFORMAT, wcs.bmformat"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Icm.h
api_name:
 - BMFORMAT
product: Windows
targetos: Windows
req.typenames: BMFORMAT
req.redist: 
---

# BMFORMAT enumeration


## -description


The values of the <b>BMFORMAT</b> enumerated type are used by several WCS functions to indicate the format that particular bitmaps are in.
        


## -enum-fields




### -field BM_x555RGB

16 bits per pixel. RGB color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555XYZ

16 bits per pixel. CIE device-independent XYZ color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555Yxy

16 bits per pixel. Yxy color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555Lab

16 bits per pixel. L*a*b color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_x555G3CH

16 bits per pixel. G3CH color space. 5 bits per channel. The most significant bit is ignored.


### -field BM_RGBTRIPLETS

24 bits per pixel maximum. For three channel colors, such as Red,Green,Blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.


### -field BM_BGRTRIPLETS

24 bits per pixel maximum. For three channel colors, such as Red,Green,Blue, the total size is 24 bits per pixel. For single channel colors, such as gray, the total size is 8 bits per pixel.


### -field BM_XYZTRIPLETS

24 bits per pixel maximum. For three channel, X, Y and Z values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/c37f821c-fb03-4b98-9ee0-c0ad7fff4685">TranslateBitmapBits</a> function does not support <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BM_XYZTRIPLETS </a> as an input.</div>
<div> </div>

### -field BM_YxyTRIPLETS

24 bits per pixel maximum. For three channel, Y, x and y values, the total size is 24 bits per pixel. For single channel gray scale, the total size is 8 bits per pixel.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/c37f821c-fb03-4b98-9ee0-c0ad7fff4685">TranslateBitmapBits</a> function does not support <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BM_YxyTRIPLETS </a> as an input.</div>
<div> </div>

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


### -field BM_xRGBQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_xBGRQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_xG3CHQUADS

32 bits per pixel. 8 bits are used for each color channel. The most significant byte is ignored.


### -field BM_KYMCQUADS

32 bits per pixel. 8 bits are used for each color channel.


### -field BM_CMYKQUADS

32 bits per pixel. 8 bits are used for each color channel.


### -field BM_10b_RGB

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_XYZ

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_Yxy

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_Lab

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_10b_G3CH

32 bits per pixel. 10 bits are used for each color channel. The 2 most significant bits are ignored.


### -field BM_NAMED_INDEX

32 bits per pixel. Named color indices. Index numbering begins at 1.


### -field BM_16b_RGB

48 bits per pixel. Each channel uses 16 bits.


### -field BM_16b_XYZ

48 bits per pixel. Each channel uses 16 bits.


### -field BM_16b_Yxy

48 bits per pixel. Each channel uses 16 bits.


### -field BM_16b_Lab

48 bits per pixel. Each channel uses 16 bits.


### -field BM_16b_G3CH

48 bits per pixel. Each channel uses 16 bits.


### -field BM_16b_GRAY

16 bits per pixel.


### -field BM_565RGB

16 bits per pixel. 5 bits are used for red, 6 for green, and 5 for blue.


### -field BM_32b_scRGB

96 bits per pixel, 32 bit per channel IEEE floating point.


### -field BM_32b_scARGB

128 bits per pixel, 32 bit per channel IEEE floating point.


### -field BM_S2DOT13FIXED_scRGB

48 bits per pixel, Fixed point integer ranging from -4 to +4 with a sign bit and 2 bit exponent and 13 bit mantissa.


### -field BM_S2DOT13FIXED_scARGB

64 bits per pixel, Fixed point integer ranging from -4 to +4 with a sign bit and 2 bit exponent and 13 bit mantissa.
          


### -field BM_R10G10B10A2

32 bits per pixel. 10 bits are used for each color channel. The two most significant bits are alpha.


### -field BM_R10G10B10A2_XR

 32 bits per pixel. 10 bits are used for each color channel. The 10 bits of each color channel are 2.8 fixed point with a -0.75 bias, giving a range of [-0.76 .. 1.25]. This range corresponds to [-0.5 .. 1.5] in a gamma = 1 space. The two most significant bits are preserved for alpha.

This uses an extended range (XR) sRGB color space. It has the same RGB primaries, white point, and gamma as sRGB.


### -field BM_R16G16B16A16_FLOAT

64 bits per pixel. Each channel is a 16-bit float. The last WORD is alpha.


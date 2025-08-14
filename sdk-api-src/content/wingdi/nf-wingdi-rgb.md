---
UID: NF:wingdi.RGB
title: RGB macro (wingdi.h)
description: The RGB macro selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.
helpviewer_keywords: ["RGB","RGB macro [Windows GDI]","_win32_RGB","gdi.rgb","wingdi/RGB"]
old-location: gdi\rgb.htm
tech.root: gdi
ms.assetid: e1dcb5f8-c026-4a4e-8541-928a057bf0ae
ms.date: 07/01/2025
ms.keywords: RGB, RGB macro [Windows GDI], _win32_RGB, gdi.rgb, wingdi/RGB
req.header: wingdi.h
req.include-header: Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RGB
 - wingdi/RGB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGB
---

# RGB macro

## -syntax

```cpp
COLORREF RGB(
    BYTE r,
    BYTE g,
    BYTE b
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

The return value is the resultant RGB color as a <a href="/windows/win32/gdi/colorref">COLORREF</a> value.


## -description

The <b>RGB</b> macro selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.

## -parameters

### -param r

The intensity of the red color.

### -param g

The intensity of the green color.

### -param b

The intensity of the blue color.

## -return

Type: <b><a href="/windows/win32/gdi/colorref">COLORREF</a></b>

The COLORREF represented by the given RGB values.

## -remarks

The intensity for each argument is in the range 0 through 255. If all three intensities are zero, the result is black. If all three intensities are 255, the result is white.

To extract the individual values for the red, green, and blue components of a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getrvalue">GetRValue</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-getgvalue">GetGValue</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-getbvalue">GetBValue</a> macros, respectively.

When creating or examining a logical palette, use the <a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a> structure to define color values and examine individual component values. For more information about using color values in a color palette, see the descriptions of the <a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-palettergb">PALETTERGB</a> macros.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbvalue">GetBValue</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getgvalue">GetGValue</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getrvalue">GetRValue</a>



<a href="/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-palettergb">PALETTERGB</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>

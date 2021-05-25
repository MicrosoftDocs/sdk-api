---
UID: NF:gdipluscolor.Color.SetFromCOLORREF
title: Color::SetFromCOLORREF (gdipluscolor.h)
description: The Color::SetFromCOLORREF method uses a Windows Graphics Device Interface (GDI)COLORREF value to set the ARGB value of this Color object.
helpviewer_keywords: ["Color class [GDI+]","SetFromCOLORREF method","Color.SetFromCOLORREF","Color::SetFromCOLORREF","SetFromCOLORREF","SetFromCOLORREF method [GDI+]","SetFromCOLORREF method [GDI+]","Color class","_gdiplus_CLASS_Color_SetFromCOLORREF_rgb_","gdiplus._gdiplus_CLASS_Color_SetFromCOLORREF_rgb_"]
old-location: gdiplus\_gdiplus_CLASS_Color_SetFromCOLORREF_rgb_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colormethods\setfromcolorref.htm
ms.date: 12/05/2018
ms.keywords: Color class [GDI+],SetFromCOLORREF method, Color.SetFromCOLORREF, Color::SetFromCOLORREF, SetFromCOLORREF, SetFromCOLORREF method [GDI+], SetFromCOLORREF method [GDI+],Color class, _gdiplus_CLASS_Color_SetFromCOLORREF_rgb_, gdiplus._gdiplus_CLASS_Color_SetFromCOLORREF_rgb_
req.header: gdipluscolor.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Color::SetFromCOLORREF
 - gdipluscolor/Color::SetFromCOLORREF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Color.SetFromCOLORREF
---

## -description

The <b>Color::SetFromCOLORREF</b> method uses a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value to set the <b>ARGB</b> value of this <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object.

## -parameters

### -param rgb [in]

Type: <b>COLORREF</b>

GDI <b>COLORREF</b> value that specifies the red, green, and blue components of this <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object's <b>ARGB</b> value. The default value of the alpha component for this <b>Color</b> object is 255.

## -remarks

A 32-bit GDI <b>COLORREF</b> value contains three, 8-bit color components. The most significant 8 bits are zeros and are not used, the next 8 bits contain the blue component, the next 8 bits contain the green component, and the last 8 bits (the least significant) contain the red component. Note that the ordering (starting with the high-order bits) of the components in a <b>COLORREF</b> value is blue, green, red; whereas, the ordering of an <b>ARGB</b> value is alpha, red, green, blue. 


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object and sets a GDI <b>COLORREF</b> value. The code then sets the <b>Color</b> object to the value of the GDI <b>COLORREF</b> value, creates a pen, and draws a line.


```cpp
VOID Example_SetFromCOLORREF(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a color object.
   Color gdipColor(255, 0, 0, 255);

   // COLORREF is defined as an unsigned long in Wingdi.h
   unsigned long gdiColorRef = RGB(0, 0, 0);   // Set a GDI COLORREF value.

   // Set the color object to the COLORREF value.
   gdipColor.SetFromCOLORREF(gdiColorRef);

   // Create a Pen object based on the Color object.
   Pen pen((gdipColor), 10);

   // Draw a line.
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-tocolorref">Color::ToCOLORREF</a>
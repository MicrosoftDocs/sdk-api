---
UID: NF:gdipluscolor.Color.ToCOLORREF
title: Color::ToCOLORREF (gdipluscolor.h)
description: The Color::ToCOLORREF method converts this Color object's ARGB value to a Windows Graphics Device Interface (GDI)COLORREF value.
helpviewer_keywords: ["Color class [GDI+]","ToCOLORREF method","Color.ToCOLORREF","Color::ToCOLORREF","ToCOLORREF","ToCOLORREF method [GDI+]","ToCOLORREF method [GDI+]","Color class","_gdiplus_CLASS_Color_ToCOLORREF_","gdiplus._gdiplus_CLASS_Color_ToCOLORREF_"]
old-location: gdiplus\_gdiplus_CLASS_Color_ToCOLORREF_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colormethods\tocolorref.htm
ms.date: 12/05/2018
ms.keywords: Color class [GDI+],ToCOLORREF method, Color.ToCOLORREF, Color::ToCOLORREF, ToCOLORREF, ToCOLORREF method [GDI+], ToCOLORREF method [GDI+],Color class, _gdiplus_CLASS_Color_ToCOLORREF_, gdiplus._gdiplus_CLASS_Color_ToCOLORREF_
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
 - Color::ToCOLORREF
 - gdipluscolor/Color::ToCOLORREF
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
 - Color.ToCOLORREF
---

# Color::ToCOLORREF


## -description

The <b>Color::ToCOLORREF</b> method converts this <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object's <b>ARGB</b> value to a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value.



## -returns

Type: <b>COLORREF</b>

This method returns a GDI <b>COLORREF</b> value that has the same red, green, and blue components as this color's <b>ARGB</b> value.

## -remarks

When the <b>ARGB</b> value is converted to a <b>COLORREF</b> value, the alpha component of the <b>ARGB</b> value is ignored.


#### Examples



The following example creates two <a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a> objects and converts the <b>ARGB</b> value of the first <b>Color</b> object into a GDI <b>COLORREF</b> value. The code then passes that <b>COLORREF</b> value to the <a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setfromcolorref">Color::SetFromCOLORREF</a> method of the second <b>Color</b> object. Finally, the code uses the second <b>Color</b> object to fill a rectangle.


```cpp
VOID Example_ToCOLORREF(HDC hdc)
{
   Graphics graphics(hdc);

   // Create two Color objects.
   Color firstColor(255, 128, 128, 255);
   Color secondColor(255, 255, 255, 255);

   // Convert the ARGB value of the first color to a COLORREF value.
   COLORREF colorRef = firstColor.ToCOLORREF();

   // Use the COLORREF value to set the color of secondColor.
   secondColor.SetFromCOLORREF(colorRef);

   // Create a SolidBrush object based on secondColor, and fill a rectangle.
   SolidBrush colorRefBrush(secondColor);
   graphics.FillRectangle(&colorRefBrush, Rect(0, 0, 100, 100));
}
```

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setfromcolorref">Color::SetFromCOLORREF</a>

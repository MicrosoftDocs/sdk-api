---
UID: NF:gdipluspen.Pen.GetWidth
title: Pen::GetWidth (gdipluspen.h)
description: The Pen::GetWidth method gets the width currently set for this Pen object.
helpviewer_keywords: ["GetWidth","GetWidth method [GDI+]","GetWidth method [GDI+]","Pen class","Pen class [GDI+]","GetWidth method","Pen.GetWidth","Pen::GetWidth","_gdiplus_CLASS_Pen_GetWidth_","gdiplus._gdiplus_CLASS_Pen_GetWidth_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetWidth_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getwidth_36.htm
ms.date: 12/05/2018
ms.keywords: GetWidth, GetWidth method [GDI+], GetWidth method [GDI+],Pen class, Pen class [GDI+],GetWidth method, Pen.GetWidth, Pen::GetWidth, _gdiplus_CLASS_Pen_GetWidth_, gdiplus._gdiplus_CLASS_Pen_GetWidth_
req.header: gdipluspen.h
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
 - Pen::GetWidth
 - gdipluspen/Pen::GetWidth
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
 - Pen.GetWidth
---

# Pen::GetWidth


## -description

The <b>Pen::GetWidth</b> method gets the width currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.



## -returns

Type: <b>REAL</b>

This method returns a real number that indicates the width of this 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -remarks

If you pass the address of a pen to one of the draw methods of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, the width of the pen's stroke is dependent on the unit of measure specified in the 
				<b>Graphics</b> object. The default unit of measure is UnitPixel, which is an element of the 
				<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a> enumeration.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object with a specified width and draws a line. The code then gets the width of the pen, creates a second pen based on the width of the first pen, and draws a second line.


```cpp
VOID Example_GetWidth(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen with a width of 15, and 
   // use that pen to draw a line.
   Pen pen(Color(255, 0, 0, 255), 15);
   graphics.DrawLine(&pen, 20, 20, 200, 100);

   // Get the width of the pen.
   REAL width = pen.GetWidth();

   // Create another pen that has the same width.
   Pen pen2(Color(255, 0, 255, 0), width);

   // Draw a second line.
   graphics.DrawLine(&pen2, 20, 60, 200, 140);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setwidth">Pen::SetWidth</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>

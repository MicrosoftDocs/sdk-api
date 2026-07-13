---
UID: NF:gdipluspen.Pen.GetPenType
title: Pen::GetPenType (gdipluspen.h)
description: The Pen::GetPenType method gets the type currently set for this Pen object.
helpviewer_keywords: ["GetPenType","GetPenType method [GDI+]","GetPenType method [GDI+]","Pen class","Pen class [GDI+]","GetPenType method","Pen.GetPenType","Pen::GetPenType","_gdiplus_CLASS_Pen_GetPenType_","gdiplus._gdiplus_CLASS_Pen_GetPenType_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetPenType_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getpentype.htm
ms.date: 12/05/2018
ms.keywords: GetPenType, GetPenType method [GDI+], GetPenType method [GDI+],Pen class, Pen class [GDI+],GetPenType method, Pen.GetPenType, Pen::GetPenType, _gdiplus_CLASS_Pen_GetPenType_, gdiplus._gdiplus_CLASS_Pen_GetPenType_
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
 - Pen::GetPenType
 - gdipluspen/Pen::GetPenType
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
 - Pen.GetPenType
---

# Pen::GetPenType


## -description

The <b>Pen::GetPenType</b> method gets the type currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pentype">PenType</a></b>

This method returns an element of the 
						<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pentype">PenType</a> enumeration that indicates the style of pen currently set for this 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -remarks

A 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object is created with a default pen type of <b>PenTypeSolidColor</b>, which is an element of the 
				<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pentype">PenType</a> enumeration.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a> object and then passes the address of that 
						<b>HatchBrush</b> object to a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> constructor. The code uses the pen, which has a width of 15, to draw a line. The code calls the <b>Pen::GetPenType</b> method to determine the pen's type, and then checks to see whether the type is PenTypeHatchFill.


```cpp
VOID Example_GetPenType(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a HatchBrush object.
   HatchBrush hatchBrush(
      HatchStyleVertical,
      Color(255, 255, 0, 0),
      Color(255, 0, 0, 255));

   // Create a pen based on a hatch brush, and use that
   // pen to draw a line.
   Pen pen(&hatchBrush, 15);
   graphics.DrawLine(&pen, 20, 20, 200, 100);

   // Obtain information about the pen.
   PenType penType = pen.GetPenType();

   if(penType == PenTypeHatchFill)
   {
      // The pen will draw with a hatch pattern.
   }
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getbrush">Pen::GetBrush</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setbrush">Pen::SetBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>

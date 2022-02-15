---
UID: NF:gdipluspen.Pen.GetAlignment
title: Pen::GetAlignment (gdipluspen.h)
description: The Pen::GetAlignment method gets the alignment currently set for this Pen object.
helpviewer_keywords: ["GetAlignment","GetAlignment method [GDI+]","GetAlignment method [GDI+]","Pen class","Pen class [GDI+]","GetAlignment method","Pen.GetAlignment","Pen::GetAlignment","_gdiplus_CLASS_Pen_GetAlignment_","gdiplus._gdiplus_CLASS_Pen_GetAlignment_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetAlignment_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getalignment.htm
ms.date: 12/05/2018
ms.keywords: GetAlignment, GetAlignment method [GDI+], GetAlignment method [GDI+],Pen class, Pen class [GDI+],GetAlignment method, Pen.GetAlignment, Pen::GetAlignment, _gdiplus_CLASS_Pen_GetAlignment_, gdiplus._gdiplus_CLASS_Pen_GetAlignment_
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
 - Pen::GetAlignment
 - gdipluspen/Pen::GetAlignment
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
 - Pen.GetAlignment
---

# Pen::GetAlignment


## -description

The <b>Pen::GetAlignment</b> method gets the alignment currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a></b>

This method returns an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a> enumeration that indicates the current alignment setting for this <a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -remarks

The default value of <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a> is PenAlignmentCenter. 


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets the alignment, draws a line, and then gets the pen alignment settings.


```cpp
VOID Example_GetAlignment(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object and set its alignment.
   Pen pen(Color(255, 0, 255, 0), 15);
   pen.SetAlignment(PenAlignmentCenter);

   // Draw a line.
   graphics.DrawLine(&pen, 0, 0, 100, 50);

   // Obtain information about the Pen object.
   PenAlignment penAlignment;
   penAlignment = pen.GetAlignment();

   if(penAlignment == PenAlignmentCenter)
      ;  // The pixels will be centered on the theoretical line.
   else if(penAlignment == PenAlignmentInset)
      ;  // The pixels will lie inside the filled area  of the theoretical line.
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setalignment">Pen::SetAlignment</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>

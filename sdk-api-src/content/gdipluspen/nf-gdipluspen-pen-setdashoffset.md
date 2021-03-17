---
UID: NF:gdipluspen.Pen.SetDashOffset
title: Pen::SetDashOffset (gdipluspen.h)
description: The Pen::SetDashOffset method sets the distance from the start of the line to the start of the first dash in a dashed line.
helpviewer_keywords: ["Pen class [GDI+]","SetDashOffset method","Pen.SetDashOffset","Pen::SetDashOffset","SetDashOffset","SetDashOffset method [GDI+]","SetDashOffset method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetDashOffset_dashOffset_","gdiplus._gdiplus_CLASS_Pen_SetDashOffset_dashOffset_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashOffset_dashOffset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashoffset.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetDashOffset method, Pen.SetDashOffset, Pen::SetDashOffset, SetDashOffset, SetDashOffset method [GDI+], SetDashOffset method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashOffset_dashOffset_, gdiplus._gdiplus_CLASS_Pen_SetDashOffset_dashOffset_
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
 - Pen::SetDashOffset
 - gdipluspen/Pen::SetDashOffset
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
 - Pen.SetDashOffset
---

# Pen::SetDashOffset


## -description

The <b>Pen::SetDashOffset</b> method sets the distance from the start of the line to the start of the first dash in a dashed line.

## -parameters

### -param dashOffset [in]

Type: <b>REAL</b>

Real number that specifies the number of times to shift the spaces in a dashed line. Each shift is equal to the length of a space in the dashed line.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A positive 
				<i>dashOffset</i> value shifts the first dash forward along the path, and a negative 
				<i>dashOffset</i> value shifts the start of the path forward along the first dash. 


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets the dash style, and draws a line. The code then sets the pen's offset value and draws a second line.


```cpp
VOID Example_SetDashOffset(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object, set the dash style, and draw a line.
   Pen pen(Color(255, 0, 0, 255), 15);
   pen.SetDashStyle(DashStyleDash);
   graphics.DrawLine(&pen, 0, 50, 400, 50);

   // Set the dash offset value for the pen, and draw a second line.
   pen.SetDashOffset(10);
   graphics.DrawLine(&pen, 0, 80, 400, 80);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashoffset">Pen::GetDashOffset</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpattern">Pen::GetDashPattern</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpatterncount">Pen::GetDashPatternCount</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashstyle">Pen::GetDashStyle</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashcap">Pen::SetDashCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashpattern">Pen::SetDashPattern</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashstyle">Pen::SetDashStyle</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
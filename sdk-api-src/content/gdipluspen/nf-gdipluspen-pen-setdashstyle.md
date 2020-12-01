---
UID: NF:gdipluspen.Pen.SetDashStyle
title: Pen::SetDashStyle (gdipluspen.h)
description: The Pen::SetDashStyle method sets the dash style for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetDashStyle method","Pen.SetDashStyle","Pen::SetDashStyle","SetDashStyle","SetDashStyle method [GDI+]","SetDashStyle method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetDashStyle_dashStyle_","gdiplus._gdiplus_CLASS_Pen_SetDashStyle_dashStyle_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashStyle_dashStyle_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashstyle.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetDashStyle method, Pen.SetDashStyle, Pen::SetDashStyle, SetDashStyle, SetDashStyle method [GDI+], SetDashStyle method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashStyle_dashStyle_, gdiplus._gdiplus_CLASS_Pen_SetDashStyle_dashStyle_
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
 - Pen::SetDashStyle
 - gdipluspen/Pen::SetDashStyle
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
 - Pen.SetDashStyle
---

# Pen::SetDashStyle


## -description

The <b>Pen::SetDashStyle</b> method sets the dash style for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param dashStyle [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashstyle">DashStyle</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashstyle">DashStyle</a> enumeration that specifies the dash style for this 
					<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The length of the dashes in a dashed line is dependent on the dash style and the width of the 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. The length of the space that separates two dashes in a dashed line is equal to the width of the 
				<b>Pen</b> object. 


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets the dash style, and draws a line. The code then resets the dash style, draws a second line, resets dash style again, and draws a third line.


```cpp
VOID Example_SetDashStyle(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen pen(Color(255, 0, 0, 255), 15);

   // Set the dash style for the pen, and draw a dashed line.
   pen.SetDashStyle(DashStyleDash);
   graphics.DrawLine(&pen, 0, 50, 400, 150);

   // Reset the dash style for the pen, and draw a second line.
   pen.SetDashStyle(DashStyleDot);
   graphics.DrawLine(&pen, 0, 80, 400, 180); 

   // Reset the dash style for the pen, and draw a third line.
   pen.SetDashStyle(DashStyleDashDot);
   graphics.DrawLine(&pen, 0, 110, 400, 210); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashcap">Pen::GetDashCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashoffset">Pen::GetDashOffset</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpattern">Pen::GetDashPattern</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpatterncount">Pen::GetDashPatternCount</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashstyle">Pen::GetDashStyle</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashcap">Pen::SetDashCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashoffset">Pen::SetDashOffset</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashpattern">Pen::SetDashPattern</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
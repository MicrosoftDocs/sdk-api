---
UID: NF:gdipluspen.Pen.SetDashCap
title: Pen::SetDashCap (gdipluspen.h)
description: The Pen::SetDashCap method sets the dash cap style for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetDashCap method","Pen.SetDashCap","Pen::SetDashCap","SetDashCap","SetDashCap method [GDI+]","SetDashCap method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetDashCap_dashCap_","gdiplus._gdiplus_CLASS_Pen_SetDashCap_dashCap_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashCap_dashCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashcap.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetDashCap method, Pen.SetDashCap, Pen::SetDashCap, SetDashCap, SetDashCap method [GDI+], SetDashCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetDashCap_dashCap_
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
 - Pen::SetDashCap
 - gdipluspen/Pen::SetDashCap
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
 - Pen.SetDashCap
---

# Pen::SetDashCap


## -description

The <b>Pen::SetDashCap</b> method sets the dash cap style for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param dashCap [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashcap">DashCap</a></b>

Element of the 
					<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashcap">DashCap</a> enumeration that specifies the dash cap for this 
					<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

If you set the alignment of a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw triangular dash caps.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets the dash style and the dash cap, and draws a dashed line.


```cpp
VOID Example_SetCustomStartCap(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen.
   Pen pen(Color(255, 0, 0, 255), 20);

   // Set the dash style for the pen.
   pen.SetDashStyle(DashStyleDash);

   // Set a triangular dash cap for the pen.
   pen.SetDashCap(DashCapTriangle);

   // Draw a line using the pen.
   graphics.DrawLine(&pen, 20, 20, 200, 100);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-line-with-line-caps-use">Drawing a Line with Line Caps</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomendcap">Pen::GetCustomEndCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomstartcap">Pen::GetCustomStartCap</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashcap">Pen::GetDashCap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
---
UID: NF:gdiplustypes.Rect.Contains(constPoint&)
title: Rect::Contains(IN const Point &) (gdiplustypes.h)
description: The Rect::Contains method determines whether a point is inside this rectangle.
helpviewer_keywords: ["Contains","Contains method [GDI+]","Contains method [GDI+]","Rect class","Rect class [GDI+]","Contains method","Rect.Contains","Rect.Contains(IN const Point &)","Rect.Contains(const Point&)","Rect::Contains","Rect::Contains(IN const Point &)","_gdiplus_CLASS_Rect_Contains_pt_","gdiplus._gdiplus_CLASS_Rect_Contains_pt_"]
old-location: gdiplus\_gdiplus_CLASS_Rect_Contains_pt_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\rectcontainsmethods\contains.htm
ms.date: 12/05/2018
ms.keywords: Contains, Contains method [GDI+], Contains method [GDI+],Rect class, Rect class [GDI+],Contains method, Rect.Contains, Rect.Contains(IN const Point &), Rect.Contains(const Point&), Rect::Contains, Rect::Contains(IN const Point &), _gdiplus_CLASS_Rect_Contains_pt_, gdiplus._gdiplus_CLASS_Rect_Contains_pt_
req.header: gdiplustypes.h
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
 - Rect::Contains
 - gdiplustypes/Rect::Contains
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
 - Rect.Contains
---

# Rect::Contains(IN const Point &)


## -description

The <b>Rect::Contains</b> method determines whether a point is inside this rectangle.

## -parameters

### -param pt [in]

Type: <b>const Point&amp;</b>

Reference to a point to be tested.

## -returns

Type: <b>BOOL</b>

If the point is inside the rectangle, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-contains(inconstpoint_)">Contains Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
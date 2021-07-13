---
UID: NF:gdiplustypes.RectF.IsEmptyArea
title: RectF::IsEmptyArea (gdiplustypes.h)
description: The RectF::IsEmptyArea method determines whether this rectangle is empty.
helpviewer_keywords: ["IsEmptyArea","IsEmptyArea method [GDI+]","IsEmptyArea method [GDI+]","RectF class","RectF class [GDI+]","IsEmptyArea method","RectF.IsEmptyArea","RectF::IsEmptyArea","_gdiplus_CLASS_RectF_IsEmptyArea_","gdiplus._gdiplus_CLASS_RectF_IsEmptyArea_"]
old-location: gdiplus\_gdiplus_CLASS_RectF_IsEmptyArea_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\isemptyarea_36.htm
ms.date: 12/05/2018
ms.keywords: IsEmptyArea, IsEmptyArea method [GDI+], IsEmptyArea method [GDI+],RectF class, RectF class [GDI+],IsEmptyArea method, RectF.IsEmptyArea, RectF::IsEmptyArea, _gdiplus_CLASS_RectF_IsEmptyArea_, gdiplus._gdiplus_CLASS_RectF_IsEmptyArea_
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
 - RectF::IsEmptyArea
 - gdiplustypes/RectF::IsEmptyArea
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
 - RectF.IsEmptyArea
---

# RectF::IsEmptyArea


## -description

The <b>RectF::IsEmptyArea</b> method determines whether this rectangle is empty.



## -returns

Type: <b>BOOL</b>

If the rectangle is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

A rectangle is defined as empty if either the width or the height is zero or less.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.


```cpp
VOID Example_IsEmptyArea(HDC hdc)
{
   Graphics graphics(hdc);
   RectF rect(50, 50, 200, 100);
   rect.Inflate(0, -120);

   if(rect.IsEmptyArea())

   // The rectangle does not enclose any area.
}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-inflate(inconstpointf_)">Inflate Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>

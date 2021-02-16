---
UID: NF:gdiplustypes.RectF.Union
title: RectF::Union (gdiplustypes.h)
description: The RectF::Union method determines the union of two rectangles and stores the result in a RectF object.
helpviewer_keywords: ["RectF class [GDI+]","Union method","RectF.Union","RectF::Union","Union","Union method [GDI+]","Union method [GDI+]","RectF class","_gdiplus_CLASS_RectF_Union_c_a_b_","gdiplus._gdiplus_CLASS_RectF_Union_c_a_b_"]
old-location: gdiplus\_gdiplus_CLASS_RectF_Union_c_a_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\union_81c_a_b.htm
ms.date: 12/05/2018
ms.keywords: RectF class [GDI+],Union method, RectF.Union, RectF::Union, Union, Union method [GDI+], Union method [GDI+],RectF class, _gdiplus_CLASS_RectF_Union_c_a_b_, gdiplus._gdiplus_CLASS_RectF_Union_c_a_b_
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
 - RectF::Union
 - gdiplustypes/RectF::Union
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
 - RectF.Union
---

# RectF::Union


## -description

The <b>RectF::Union</b> method determines the union of two rectangles and stores the result in a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object.

## -parameters

### -param c [out]

Type: <b>RectF&amp;</b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a> object that receives the union of the two rectangles.

### -param a [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles used to form the union.

### -param b [in]

Type: <b>const RectF&amp;</b>

Reference to one of the two rectangles used to form the union.

## -returns

Type: <b>BOOL</b>

If the union of two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

In GDI+, the union of two rectangles is the smallest rectangle that encloses the two rectangles. A rectangle is defined as empty if its width or height is less than or equal to zero.


#### Examples



The following example creates three rectangles. The code forms the union of the first two rectangles and stores the result in the third rectangle. The code determines whether the union is nonempty and, if so, draws the union.


```cpp
VOID Example_UnionABC(HDC hdc)
{
   Graphics graphics(hdc);
   Pen* pGreenPen;

   // Create three RectF objects.
   RectF rectA(50, 50, 200, 100);
   RectF rectB(70, 20, 100, 200);
   RectF rectC;

   // Determine the union of rectA and rectB, and store the result in rectC.
   if(rectC.Union(rectC, rectA, rectB))
   {
      // rectC is not empty.
      // Draw the union with a thick green pen.
      pGreenPen = new Pen(Color(255, 0, 255, 0), 7);
      graphics.DrawRectangle(pGreenPen, rectC);
      delete pGreenPen;
   }
   // Draw rectA and rectB with a thin black pen.
   Pen blackPen(Color(255, 0, 0, 0), 1);
   graphics.DrawRectangle(&blackPen, rectA);
   graphics.DrawRectangle(&blackPen, rectB);}
```

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersect(outrectf__inconstrectf__inconstrectf_)">Intersect Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
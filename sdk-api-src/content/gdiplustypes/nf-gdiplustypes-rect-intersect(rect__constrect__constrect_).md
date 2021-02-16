---
UID: NF:gdiplustypes.Rect.Intersect(Rect&,constRect&,constRect&)
title: Rect::Intersect(OUT Rect &,IN const Rect &,IN const Rect &) (gdiplustypes.h)
description: The Rect::Intersect method determines the intersection of two rectangles and stores the result in a Rect object.
helpviewer_keywords: ["Intersect","Intersect method [GDI+]","Intersect method [GDI+]","Rect class","Rect class [GDI+]","Intersect method","Rect.Intersect","Rect.Intersect(OUT Rect &","IN const Rect &","IN const Rect &)","Rect.Intersect(Rect&","const Rect&","const Rect&)","Rect::Intersect","Rect::Intersect(OUT Rect &","IN const Rect &","IN const Rect &)","_gdiplus_CLASS_Rect_Intersect_c_a_b_","gdiplus._gdiplus_CLASS_Rect_Intersect_c_a_b_"]
old-location: gdiplus\_gdiplus_CLASS_Rect_Intersect_c_a_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\rectintersectmethods\intersect.htm
ms.date: 12/05/2018
ms.keywords: Intersect, Intersect method [GDI+], Intersect method [GDI+],Rect class, Rect class [GDI+],Intersect method, Rect.Intersect, Rect.Intersect(OUT Rect &,IN const Rect &,IN const Rect &), Rect.Intersect(Rect&,const Rect&,const Rect&), Rect::Intersect, Rect::Intersect(OUT Rect &,IN const Rect &,IN const Rect &), _gdiplus_CLASS_Rect_Intersect_c_a_b_, gdiplus._gdiplus_CLASS_Rect_Intersect_c_a_b_
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
 - Rect::Intersect
 - gdiplustypes/Rect::Intersect
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
 - Rect.Intersect
---

# Rect::Intersect(OUT Rect &,IN const Rect &,IN const Rect &)


## -description

The <b>Rect::Intersect</b> method determines the intersection of two rectangles and stores the result in a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object.

## -parameters

### -param c [out]

Type: <b>Rect&amp;</b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a> object that receives the intersection of the two rectangles.

### -param a [in]

Type: <b>const Rect&amp;</b>

Reference to one of the two rectangles to be intersected.

### -param b [in]

Type: <b>const Rect&amp;</b>

Reference to one of the two rectangles to be intersected.

## -returns

Type: <b>BOOL</b>

If the intersection of the two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersect(outrect__inconstrect__inconstrect_)">Intersect Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
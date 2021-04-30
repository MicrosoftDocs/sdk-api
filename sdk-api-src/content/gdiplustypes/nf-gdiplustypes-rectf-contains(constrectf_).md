---
UID: NF:gdiplustypes.RectF.Contains(constRectF&)
title: RectF::Contains(IN const RectF &) (gdiplustypes.h)
description: The RectF::Contains method determines whether another rectangle is inside this rectangle.
helpviewer_keywords: ["Contains","Contains method [GDI+]","Contains method [GDI+]","RectF class","RectF class [GDI+]","Contains method","RectF.Contains","RectF.Contains(IN const RectF &)","RectF.Contains(const RectF&)","RectF::Contains","RectF::Contains(IN const RectF &)","_gdiplus_CLASS_RectF_Contains_rect_","gdiplus._gdiplus_CLASS_RectF_Contains_rect_"]
old-location: gdiplus\_gdiplus_CLASS_RectF_Contains_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\rectfcontainsmethods\contains_10rect.htm
ms.date: 12/05/2018
ms.keywords: Contains, Contains method [GDI+], Contains method [GDI+],RectF class, RectF class [GDI+],Contains method, RectF.Contains, RectF.Contains(IN const RectF &), RectF.Contains(const RectF&), RectF::Contains, RectF::Contains(IN const RectF &), _gdiplus_CLASS_RectF_Contains_rect_, gdiplus._gdiplus_CLASS_RectF_Contains_rect_
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
 - RectF::Contains
 - gdiplustypes/RectF::Contains
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
 - RectF.Contains
---

# RectF::Contains(IN const RectF &)


## -description

The <b>RectF::Contains</b> method determines whether another rectangle is inside this rectangle.

## -parameters

### -param rect [in]

Type: <b>const RectF&amp;</b>

Reference to a rectangle to test against this rectangle.

## -returns

Type: <b>BOOL</b>

If the rectangle is inside this rectangle, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-contains(inconstpointf_)">Contains Methods</a>



<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersect(outrectf__inconstrectf__inconstrectf_)">Intersect Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersectswith">RectF::IntersectsWith</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
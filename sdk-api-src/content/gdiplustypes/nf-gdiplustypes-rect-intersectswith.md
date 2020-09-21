---
UID: NF:gdiplustypes.Rect.IntersectsWith
title: Rect::IntersectsWith (gdiplustypes.h)
description: The Rect::IntersectsWith method determines whether this rectangle intersects another rectangle.
helpviewer_keywords: ["IntersectsWith","IntersectsWith method [GDI+]","IntersectsWith method [GDI+]","Rect class","Rect class [GDI+]","IntersectsWith method","Rect.IntersectsWith","Rect::IntersectsWith","_gdiplus_CLASS_Rect_IntersectsWith_rect_","gdiplus._gdiplus_CLASS_Rect_IntersectsWith_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Rect_IntersectsWith_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectclass\rectmethods\intersectswith.htm
ms.date: 12/05/2018
ms.keywords: IntersectsWith, IntersectsWith method [GDI+], IntersectsWith method [GDI+],Rect class, Rect class [GDI+],IntersectsWith method, Rect.IntersectsWith, Rect::IntersectsWith, _gdiplus_CLASS_Rect_IntersectsWith_rect_, gdiplus._gdiplus_CLASS_Rect_IntersectsWith_rect_
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
 - Rect::IntersectsWith
 - gdiplustypes/Rect::IntersectsWith
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
 - Rect.IntersectsWith
---

# Rect::IntersectsWith


## -description

The <b>Rect::IntersectsWith</b> method determines whether this rectangle intersects another rectangle.

## -parameters

### -param rect [in]

Type: <b>const Rect&amp;</b>

Reference to a rectangle to test.

## -returns

Type: <b>BOOL</b>

If the intersection of the two rectangles is not empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersect(outrect__inconstrect__inconstrect_)">Intersect Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
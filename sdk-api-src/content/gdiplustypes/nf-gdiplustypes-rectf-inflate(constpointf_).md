---
UID: NF:gdiplustypes.RectF.Inflate(constPointF&)
title: RectF::Inflate(IN const PointF &) (gdiplustypes.h)
description: The RectF::Inflate method expands the rectangle by the value of point.X on the left and right edges, and by the value of point.Y on the top and bottom edges.
helpviewer_keywords: ["Inflate","Inflate method [GDI+]","Inflate method [GDI+]","RectF class","RectF class [GDI+]","Inflate method","RectF.Inflate","RectF.Inflate(IN const PointF &)","RectF.Inflate(const PointF&)","RectF::Inflate","RectF::Inflate(IN const PointF &)","_gdiplus_CLASS_RectF_Inflate_point_","gdiplus._gdiplus_CLASS_RectF_Inflate_point_"]
old-location: gdiplus\_gdiplus_CLASS_RectF_Inflate_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectfclass\rectfmethods\rectfinflatemethods\inflate_61point.htm
ms.date: 12/05/2018
ms.keywords: Inflate, Inflate method [GDI+], Inflate method [GDI+],RectF class, RectF class [GDI+],Inflate method, RectF.Inflate, RectF.Inflate(IN const PointF &), RectF.Inflate(const PointF&), RectF::Inflate, RectF::Inflate(IN const PointF &), _gdiplus_CLASS_RectF_Inflate_point_, gdiplus._gdiplus_CLASS_RectF_Inflate_point_
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
 - RectF::Inflate
 - gdiplustypes/RectF::Inflate
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
 - RectF.Inflate
---

# RectF::Inflate(IN const PointF &)


## -description

The <b>RectF::Inflate</b> method expands the rectangle by the value of 
			<i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

## -parameters

### -param point [in]

Type: <b>const PointF&amp;</b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object whose 
					<b>X</b> data member specifies the amount to expand the rectangle on the left and right edges, and whose 
					<b>Y</b> data member specifies the amount to expand the rectangle on the top and bottom edges.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
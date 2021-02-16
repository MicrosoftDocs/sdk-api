---
UID: NF:gdipluspath.GraphicsPath.AddRectangles(constRect,INT)
title: GraphicsPath::AddRectangles(IN const Rect,INT) (gdipluspath.h)
description: The GraphicsPath::AddRectangles method adds a sequence of rectangles to this path
helpviewer_keywords: ["AddRectangles","AddRectangles method [GDI+]","AddRectangles method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddRectangles method","GraphicsPath.AddRectangles","GraphicsPath.AddRectangles(IN const Rect","INT)","GraphicsPath.AddRectangles(const Rect*","INT)","GraphicsPath::AddRectangles","GraphicsPath::AddRectangles(IN const Rect","INT)","_gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_","gdiplus._gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddrectanglesmethods\addrectangles.htm
ms.date: 12/05/2018
ms.keywords: AddRectangles, AddRectangles method [GDI+], AddRectangles method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddRectangles method, GraphicsPath.AddRectangles, GraphicsPath.AddRectangles(IN const Rect,INT), GraphicsPath.AddRectangles(const Rect*,INT), GraphicsPath::AddRectangles, GraphicsPath::AddRectangles(IN const Rect,INT), _gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddRectangles_Rect_rects_INT_count_
req.header: gdipluspath.h
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
 - GraphicsPath::AddRectangles
 - gdipluspath/GraphicsPath::AddRectangles
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
 - GraphicsPath.AddRectangles
---

# GraphicsPath::AddRectangles(IN const Rect,INT)


## -description

The <b>GraphicsPath::AddRectangles</b> method adds a sequence of rectangles to this path

## -parameters

### -param rects [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>*</b>

Pointer to an array of rectangles that will be added to the path.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>rects</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrect_)">AddRectangle Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrect_int)">AddRectangles Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>
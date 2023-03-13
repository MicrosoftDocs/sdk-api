---
UID: NF:gdipluspath.GraphicsPath.AddLine(constPoint&,constPoint&)
title: GraphicsPath::AddLine(IN const Point &,IN const Point &) (gdipluspath.h)
description: The GraphicsPath::AddLine method adds a line to the current figure of this path. (overload 2/4)
helpviewer_keywords: ["AddLine","AddLine method [GDI+]","AddLine method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddLine method","GraphicsPath.AddLine","GraphicsPath.AddLine(IN const Point &","IN const Point &)","GraphicsPath.AddLine(const Point&","const Point&)","GraphicsPath::AddLine","GraphicsPath::AddLine(IN const Point &","IN const Point &)","_gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_","gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinemethods\addline.htm
ms.date: 12/05/2018
ms.keywords: AddLine, AddLine method [GDI+], AddLine method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLine method, GraphicsPath.AddLine, GraphicsPath.AddLine(IN const Point &,IN const Point &), GraphicsPath.AddLine(const Point&,const Point&), GraphicsPath::AddLine, GraphicsPath::AddLine(IN const Point &,IN const Point &), _gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_Point_pt1_Point_pt2_
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
 - GraphicsPath::AddLine
 - gdipluspath/GraphicsPath::AddLine
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
 - GraphicsPath.AddLine
---

# GraphicsPath::AddLine(IN const Point &,IN const Point &)


## -description

The <b>GraphicsPath::AddLine</b> method adds a line to the current figure of this path.

## -parameters

### -param pt1 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point at which to start the line.

### -param pt2 [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a point at which to end the line.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inconstpoint__inconstpoint_)">AddLine Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)">AddLines Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>

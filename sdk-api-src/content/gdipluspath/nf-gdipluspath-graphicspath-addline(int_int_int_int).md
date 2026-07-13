---
UID: NF:gdipluspath.GraphicsPath.AddLine(INT,INT,INT,INT)
title: GraphicsPath::AddLine(IN INT,IN INT,IN INT,IN INT) (gdipluspath.h)
description: The GraphicsPath::AddLine method adds a line to the current figure of this path. (overload 3/4)
helpviewer_keywords: ["AddLine","AddLine method [GDI+]","AddLine method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddLine method","GraphicsPath.AddLine","GraphicsPath.AddLine(IN INT","IN INT","IN INT","IN INT)","GraphicsPath.AddLine(INT","INT","INT","INT)","GraphicsPath::AddLine","GraphicsPath::AddLine(IN INT","IN INT","IN INT","IN INT)","_gdiplus_CLASS_GraphicsPath_AddLine_INT_x1_INT_y1_INT_x2_INT_y2_","gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_INT_x1_INT_y1_INT_x2_INT_y2_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddLine_INT_x1_INT_y1_INT_x2_INT_y2_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddlinemethods\addline_82intx1_inty1_intx2_inty2.htm
ms.date: 12/05/2018
ms.keywords: AddLine, AddLine method [GDI+], AddLine method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddLine method, GraphicsPath.AddLine, GraphicsPath.AddLine(IN INT,IN INT,IN INT,IN INT), GraphicsPath.AddLine(INT,INT,INT,INT), GraphicsPath::AddLine, GraphicsPath::AddLine(IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_GraphicsPath_AddLine_INT_x1_INT_y1_INT_x2_INT_y2_, gdiplus._gdiplus_CLASS_GraphicsPath_AddLine_INT_x1_INT_y1_INT_x2_INT_y2_
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

# GraphicsPath::AddLine(IN INT,IN INT,IN INT,IN INT)


## -description

The <b>GraphicsPath::AddLine</b> method adds a line to the current figure of this path.

## -parameters

### -param x1 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the starting point of the line.

### -param y1 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the starting point of the line.

### -param x2 [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the ending point of the line.

### -param y2 [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the ending point of the line.

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



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use">Using a Pen to Draw Lines and Rectangles</a>

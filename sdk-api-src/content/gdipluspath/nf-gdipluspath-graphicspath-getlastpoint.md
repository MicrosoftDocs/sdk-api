---
UID: NF:gdipluspath.GraphicsPath.GetLastPoint
title: GraphicsPath::GetLastPoint (gdipluspath.h)
description: The GraphicsPath::GetLastPoint method gets the ending point of the last figure in this path.
helpviewer_keywords: ["GetLastPoint","GetLastPoint method [GDI+]","GetLastPoint method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","GetLastPoint method","GraphicsPath.GetLastPoint","GraphicsPath::GetLastPoint","_gdiplus_CLASS_GraphicsPath_GetLastPoint_lastPoint_","gdiplus._gdiplus_CLASS_GraphicsPath_GetLastPoint_lastPoint_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetLastPoint_lastPoint_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getlastpoint.htm
ms.date: 12/05/2018
ms.keywords: GetLastPoint, GetLastPoint method [GDI+], GetLastPoint method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetLastPoint method, GraphicsPath.GetLastPoint, GraphicsPath::GetLastPoint, _gdiplus_CLASS_GraphicsPath_GetLastPoint_lastPoint_, gdiplus._gdiplus_CLASS_GraphicsPath_GetLastPoint_lastPoint_
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
 - GraphicsPath::GetLastPoint
 - gdipluspath/GraphicsPath::GetLastPoint
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
 - GraphicsPath.GetLastPoint
---

# GraphicsPath::GetLastPoint


## -description

The <b>GraphicsPath::GetLastPoint</b> method gets the ending point of the last figure in this path.

## -parameters

### -param lastPoint [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that receives the last point.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)">AddLines Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>
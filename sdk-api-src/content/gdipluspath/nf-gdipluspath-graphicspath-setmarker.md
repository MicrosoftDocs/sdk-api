---
UID: NF:gdipluspath.GraphicsPath.SetMarker
title: GraphicsPath::SetMarker (gdipluspath.h)
description: The GraphicsPath::SetMarker method designates the last point in this path as a marker point.
helpviewer_keywords: ["GraphicsPath class [GDI+]","SetMarker method","GraphicsPath.SetMarker","GraphicsPath::SetMarker","SetMarker","SetMarker method [GDI+]","SetMarker method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_SetMarker_","gdiplus._gdiplus_CLASS_GraphicsPath_SetMarker_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_SetMarker_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\setmarker.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],SetMarker method, GraphicsPath.SetMarker, GraphicsPath::SetMarker, SetMarker, SetMarker method [GDI+], SetMarker method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_SetMarker_, gdiplus._gdiplus_CLASS_GraphicsPath_SetMarker_
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
 - GraphicsPath::SetMarker
 - gdipluspath/GraphicsPath::SetMarker
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
 - GraphicsPath.SetMarker
---

# GraphicsPath::SetMarker


## -description

The <b>GraphicsPath::SetMarker</b> method designates the last point in this path as a marker point.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

A <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

Each time you add a line, curve, or shape to a path, the point array and the type array are expanded. When you call <b>GraphicsPath::SetMarker</b>, a marker flag is placed in the last byte of the type array. That flag designates the last point of the point array as a marker point.

Markers divide a path into sections. You can use a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> object to draw selected sections of a path.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-closefigure">GraphicsPath::CloseFigure</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-startfigure">GraphicsPath::StartFigure</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">GraphicsPathIterator::NextSubpath Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>

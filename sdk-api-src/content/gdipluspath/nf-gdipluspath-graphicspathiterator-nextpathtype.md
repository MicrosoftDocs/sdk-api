---
UID: NF:gdipluspath.GraphicsPathIterator.NextPathType
title: GraphicsPathIterator::NextPathType (gdipluspath.h)
description: The GraphicsPathIterator::NextPathType method gets the starting index and the ending index of the next group of data points that all have the same type.
helpviewer_keywords: ["GraphicsPathIterator class [GDI+]","NextPathType method","GraphicsPathIterator.NextPathType","GraphicsPathIterator::NextPathType","NextPathType","NextPathType method [GDI+]","NextPathType method [GDI+]","GraphicsPathIterator class","_gdiplus_CLASS_GraphicsPathIterator_NextPathType_pathType_startIndex_endIndex_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextPathType_pathType_startIndex_endIndex_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_NextPathType_pathType_startIndex_endIndex_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\nextpathtype.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],NextPathType method, GraphicsPathIterator.NextPathType, GraphicsPathIterator::NextPathType, NextPathType, NextPathType method [GDI+], NextPathType method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_NextPathType_pathType_startIndex_endIndex_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextPathType_pathType_startIndex_endIndex_
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
 - GraphicsPathIterator::NextPathType
 - gdipluspath/GraphicsPathIterator::NextPathType
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
 - GraphicsPathIterator.NextPathType
---

# GraphicsPathIterator::NextPathType


## -description

The <b>GraphicsPathIterator::NextPathType</b> method gets the starting index and the ending index of the next group of data points that all have the same type.

## -parameters

### -param pathType [out]

Type: <b>BYTE*</b>

Pointer to a <b>BYTE</b> that receives the point type shared by all points in the group. Possible values are PathPointTypeLine and PathPointTypeBezier, which are elements of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a> enumeration.

### -param startIndex [out]

Type: <b>INT*</b>

Pointer to an <b>INT</b> that receives the starting index of the group of points.

### -param endIndex [out]

Type: <b>INT*</b>

Pointer to an <b>INT</b> that receives the ending index of the group of points.

## -returns

Type: <b>INT</b>

This method returns the number of data points in the group. If there are no more groups in the path, this method returns 0.

## -remarks

A path has an array of data points that define its lines and curves. All curves in the path are represented as Bézier splines, so a given point in the array has one of two types: PathPointTypeLine or PathPointTypeBezier.

The first time you call the <a href="/previous-versions/ms535462(v=vs.85)">GraphicsPathIterator::NextSubpath</a> method of an iterator, it gets the starting and ending indices of the first group of points that all have the same type. The second time, it gets the second group, and so on. Each time you call <b>GraphicsPathIterator::NextSubpath</b>, it returns the number of data points in the obtained group. When there are no groups remaining, it returns 0.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath)">GraphicsPathIterator::NextMarker Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool)">GraphicsPathIterator::NextSubpath Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>
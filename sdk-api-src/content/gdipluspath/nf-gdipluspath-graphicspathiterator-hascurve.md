---
UID: NF:gdipluspath.GraphicsPathIterator.HasCurve
title: GraphicsPathIterator::HasCurve (gdipluspath.h)
description: The GraphicsPathIterator::HasCurve method determines whether the path has any curves.
helpviewer_keywords: ["GraphicsPathIterator class [GDI+]","HasCurve method","GraphicsPathIterator.HasCurve","GraphicsPathIterator::HasCurve","HasCurve","HasCurve method [GDI+]","HasCurve method [GDI+]","GraphicsPathIterator class","_gdiplus_CLASS_GraphicsPathIterator_HasCurve_","gdiplus._gdiplus_CLASS_GraphicsPathIterator_HasCurve_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_HasCurve_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\hascurve.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],HasCurve method, GraphicsPathIterator.HasCurve, GraphicsPathIterator::HasCurve, HasCurve, HasCurve method [GDI+], HasCurve method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_HasCurve_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_HasCurve_
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
 - GraphicsPathIterator::HasCurve
 - gdipluspath/GraphicsPathIterator::HasCurve
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
 - GraphicsPathIterator.HasCurve
---

# GraphicsPathIterator::HasCurve


## -description

The <b>GraphicsPathIterator::HasCurve</b> method determines whether the path has any curves.



## -returns

Type: <b>BOOL</b>

If the path has at least one curve, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

All curves in a path are stored as sequences of Bézier splines. For example, when you add an ellipse to a path, you specify the upper-left corner, the width, and the height of the ellipse's bounding rectangle. Those numbers (upper-left corner, width, and height) are not stored in the path; instead; the ellipse is converted to a sequence of four Bézier splines. The path stores the endpoints and control points of those Bézier splines.

A path stores an array of data points, each of which belongs to a line or a Bézier spline. If some of the points in the array belong to Bézier splines, then <b>GraphicsPathIterator::HasCurve</b> returns <b>TRUE</b>. If all points in the array belong to lines, then <b>GraphicsPathIterator::HasCurve</b> returns <b>FALSE</b>.

Certain methods flatten a path, which means that all the curves in the path are converted to sequences of lines. After a path has been flattened, <b>GraphicsPathIterator::HasCurve</b> will always return <b>FALSE</b>. Flattening happens when you call the <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-flatten">Flatten</a>, <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-widen">Widen</a>, or <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-warp">Warp</a> method of the <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> class.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-flatten">Flatten</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-copydata">GraphicsPathIterator::CopyData</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-warp">Warp</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-widen">Widen</a>

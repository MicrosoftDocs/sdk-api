---
UID: NF:gdipluspath.GraphicsPathIterator.HasCurve
title: GraphicsPathIterator::HasCurve (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPathIterator::HasCurve method determines whether the path has any curves.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_HasCurve_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\hascurve.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator class [GDI+],HasCurve method, GraphicsPathIterator.HasCurve, GraphicsPathIterator::HasCurve, HasCurve, HasCurve method [GDI+], HasCurve method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_HasCurve_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_HasCurve_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPathIterator.HasCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::HasCurve


## -description


The <b>GraphicsPathIterator::HasCurve</b> method determines whether the path has any curves.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the path has at least one curve, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



All curves in a path are stored as sequences of Bézier splines. For example, when you add an ellipse to a path, you specify the upper-left corner, the width, and the height of the ellipse's bounding rectangle. Those numbers (upper-left corner, width, and height) are not stored in the path; instead; the ellipse is converted to a sequence of four Bézier splines. The path stores the endpoints and control points of those Bézier splines.

A path stores an array of data points, each of which belongs to a line or a Bézier spline. If some of the points in the array belong to Bézier splines, then <b>GraphicsPathIterator::HasCurve</b> returns <b>TRUE</b>. If all points in the array belong to lines, then <b>GraphicsPathIterator::HasCurve</b> returns <b>FALSE</b>.

Certain methods flatten a path, which means that all the curves in the path are converted to sequences of lines. After a path has been flattened, <b>GraphicsPathIterator::HasCurve</b> will always return <b>FALSE</b>. Flattening happens when you call the <a href="https://msdn.microsoft.com/en-us/library/ms535530(v=VS.85).aspx">Flatten</a>, <a href="https://msdn.microsoft.com/en-us/library/ms535572(v=VS.85).aspx">Widen</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms535571(v=VS.85).aspx">Warp</a> method of the <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> class.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535530(v=VS.85).aspx">Flatten</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535452(v=VS.85).aspx">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535571(v=VS.85).aspx">Warp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535572(v=VS.85).aspx">Widen</a>
 

 


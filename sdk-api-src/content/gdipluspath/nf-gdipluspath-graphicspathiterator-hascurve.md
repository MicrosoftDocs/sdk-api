---
UID: NF:gdipluspath.GraphicsPathIterator.HasCurve
title: GraphicsPathIterator::HasCurve
author: windows-driver-content
description: The GraphicsPathIterator::HasCurve method determines whether the path has any curves.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_HasCurve_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\hascurve.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GraphicsPathIterator class [GDI+],HasCurve method, GraphicsPathIterator.HasCurve, GraphicsPathIterator::HasCurve, HasCurve, HasCurve method [GDI+], HasCurve method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_HasCurve_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_HasCurve_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	GraphicsPathIterator.HasCurve
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
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

Certain methods flatten a path, which means that all the curves in the path are converted to sequences of lines. After a path has been flattened, <b>GraphicsPathIterator::HasCurve</b> will always return <b>FALSE</b>. Flattening happens when you call the <a href="https://msdn.microsoft.com/947b3e68-67ad-47fb-80bb-b5a678f71381">Flatten</a>, <a href="https://msdn.microsoft.com/e8351fb1-b11f-4da7-9cc4-dc3ab685f29d">Widen</a>, or <a href="https://msdn.microsoft.com/7c7931ab-f8fd-46f9-a140-9e680bf06002">Warp</a> method of the <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> class.




## -see-also




<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/947b3e68-67ad-47fb-80bb-b5a678f71381">Flatten</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/6b58521e-3093-45c7-93b4-ca658b67601f">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/7c7931ab-f8fd-46f9-a140-9e680bf06002">Warp</a>



<a href="https://msdn.microsoft.com/e8351fb1-b11f-4da7-9cc4-dc3ab685f29d">Widen</a>
 

 


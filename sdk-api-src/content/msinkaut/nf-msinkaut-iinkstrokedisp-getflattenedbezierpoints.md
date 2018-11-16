---
UID: NF:msinkaut.IInkStrokeDisp.GetFlattenedBezierPoints
title: IInkStrokeDisp::GetFlattenedBezierPoints
author: windows-sdk-content
description: Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or a InkStrokes collection.
old-location: tablet\iinkstrokedisp_getflattenedbezierpoints.htm
tech.root: tablet
ms.assetid: e39e3fc3-bcdc-4d88-8051-18ed8b183c79
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFlattenedBezierPoints, GetFlattenedBezierPoints method [Tablet PC], GetFlattenedBezierPoints method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetFlattenedBezierPoints method, IInkStrokeDisp.GetFlattenedBezierPoints, IInkStrokeDisp::GetFlattenedBezierPoints, e39e3fc3-bcdc-4d88-8051-18ed8b183c79, msinkaut/IInkStrokeDisp::GetFlattenedBezierPoints, tablet.iinkstrokedisp_getflattenedbezierpoints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokeDisp.GetFlattenedBezierPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkStrokeDisp.GetFlattenedBezierPoints
: 
---

# IInkStrokeDisp::GetFlattenedBezierPoints


## -description



Retrieves the bounding box in <b>ink space</b> coordinates for either all of the strokes in an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, an individual stroke, or a <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.




## -parameters




### -param FittingError [in, optional]

Optional. The maximum distance (accuracy), using ink space units, between the Bezier control points and the points of the stroke. This is also known as the curve fitting error level. The default value is 0.


### -param FlattenedBezierPoints [out, retval]

When this method returns, contains a point array that indicates the points that were used to draw the Bezier curve representation of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object. The Variant result contains an array in the form x1, y1, x2, y2, and so on, of the Bezier points.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_STROKE</b></dt>
</dl>
</td>
<td width="60%">
The stroke is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate Stroke handler helper object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The fitting error was out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -remarks



You should ideally set the <i>fittingError</i> parameter between 0 and 500. If the value is greater than 500, a stroke may appear distorted or coarse when drawn. Strokes appear smoothest when the fitting error level is set to 0, but the drawing performance is slowest at this level.




## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/76bb749d-76cd-4c40-add3-4065d46ed6cb">IInkStrokeDisp::BezierPoints Property</a>
 

 


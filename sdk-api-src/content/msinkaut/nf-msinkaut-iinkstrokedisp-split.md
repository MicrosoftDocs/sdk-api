---
UID: NF:msinkaut.IInkStrokeDisp.Split
title: IInkStrokeDisp::Split (msinkaut.h)
description: Splits the stroke at the specified location on the stroke.
helpviewer_keywords: ["1ae627e9-c546-485a-880c-e59d2191884d","IInkStrokeDisp interface [Tablet PC]","Split method","IInkStrokeDisp.Split","IInkStrokeDisp::Split","Split","Split method [Tablet PC]","Split method [Tablet PC]","IInkStrokeDisp interface","msinkaut/IInkStrokeDisp::Split","tablet.iinkstrokedisp_split"]
old-location: tablet\iinkstrokedisp_split.htm
tech.root: tablet
ms.assetid: 1ae627e9-c546-485a-880c-e59d2191884d
ms.date: 12/05/2018
ms.keywords: 1ae627e9-c546-485a-880c-e59d2191884d, IInkStrokeDisp interface [Tablet PC],Split method, IInkStrokeDisp.Split, IInkStrokeDisp::Split, Split, Split method [Tablet PC], Split method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::Split, tablet.iinkstrokedisp_split
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokeDisp::Split
 - msinkaut/IInkStrokeDisp::Split
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokeDisp.Split
---

# IInkStrokeDisp::Split


## -description

Splits the stroke at the specified location on the stroke.

## -parameters

### -param SplitAt [in]

The floating point index value that represents where to split the stroke.

<div class="alert"><b>Note</b>  A floating point index is a float value that represents a location somewhere between two points in the stroke. As examples, if 0.0 is the first point in the stroke and 1.0 is the second point in the stroke, 0.5 is halfway between the first and second points. Similarly, a floating point index value of 37.25 represents a location that is 25 percent along the line between points 37 and 38 of the stroke.</div>
<div> </div>

### -param NewStroke [out, retval]

When this method returns, contains a pointer to the new <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object that is created from the split operation.

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
The parameter is invalid.

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
</table>

## -remarks

This method inserts the new stroke immediately after the original stroke in the stroke set and renumbers the remaining stroke indices.

When an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> is split, the beginning portion of the stroke remains the ID of the original <b>IInkStrokeDisp</b>. The end portion of the <b>IInkStrokeDisp</b> becomes a new <b>IInkStrokeDisp</b> with an ID that is one greater than the highest <b>IInkStrokeDisp</b> ID. If the original <b>IInkStrokeDisp</b> was in an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection (other than the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Ink.Strokes</a>), only the beginning portion remains in that collection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>
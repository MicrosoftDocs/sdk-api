---
UID: NF:msinkaut.IInkStrokeDisp.Transform
title: IInkStrokeDisp::Transform (msinkaut.h)
description: Applies a linear transformation to an IInkStrokeDisp object or an InkStrokes collection, which can represent scaling, rotation, translation, and combinations of transformations. (IInkStrokeDisp.Transform)
helpviewer_keywords: ["IInkStrokeDisp interface [Tablet PC]","Transform method","IInkStrokeDisp.Transform","IInkStrokeDisp::Transform","Transform","Transform method [Tablet PC]","Transform method [Tablet PC]","IInkStrokeDisp interface","b7860215-a267-407e-9105-8e51340f4216","msinkaut/IInkStrokeDisp::Transform","tablet.iinkstrokedisp_transform"]
old-location: tablet\iinkstrokedisp_transform.htm
tech.root: tablet
ms.assetid: b7860215-a267-407e-9105-8e51340f4216
ms.date: 12/05/2018
ms.keywords: IInkStrokeDisp interface [Tablet PC],Transform method, IInkStrokeDisp.Transform, IInkStrokeDisp::Transform, Transform, Transform method [Tablet PC], Transform method [Tablet PC],IInkStrokeDisp interface, b7860215-a267-407e-9105-8e51340f4216, msinkaut/IInkStrokeDisp::Transform, tablet.iinkstrokedisp_transform
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
 - IInkStrokeDisp::Transform
 - msinkaut/IInkStrokeDisp::Transform
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
 - IInkStrokeDisp.Transform
---

# IInkStrokeDisp::Transform


## -description

Applies a linear transformation to an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection, which can represent scaling, rotation, translation, and combinations of transformations.

## -parameters

### -param Transform [in]

The transform to use on the stroke or strokes. (This is an <a href="/windows/desktop/tablet/inktransform-class">InkTransform</a> object, which correlates to the <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure). The transformation applies to both the points and pen width (if <i>ApplyOnPenWidth</i> is <b>VARIANT_TRUE</b>).

### -param ApplyOnPenWidth [in, optional]

Optional. <b>VARIANT_TRUE</b> to apply the transform to the width of the ink in the <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> of the strokes; otherwise, <b>VARIANT_FALSE</b>. The default is <b>VARIANT_FALSE</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>

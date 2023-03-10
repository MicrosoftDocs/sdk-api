---
UID: NF:msinkaut.IInkDrawingAttributes.Clone
title: IInkDrawingAttributes::Clone (msinkaut.h)
description: Creates a duplicate InkDrawingAttributes object.
helpviewer_keywords: ["Clone","Clone method [Tablet PC]","Clone method [Tablet PC]","IInkDrawingAttributes interface","IInkDrawingAttributes interface [Tablet PC]","Clone method","IInkDrawingAttributes.Clone","IInkDrawingAttributes::Clone","f3ec6b42-2b5d-459e-ba09-88c27b125c40","msinkaut/IInkDrawingAttributes::Clone","tablet.inkdrawingattributes_clone"]
old-location: tablet\inkdrawingattributes_clone.htm
tech.root: tablet
ms.assetid: 97facd95-af49-459e-82fc-12534d466786
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Tablet PC], Clone method [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],Clone method, IInkDrawingAttributes.Clone, IInkDrawingAttributes::Clone, f3ec6b42-2b5d-459e-ba09-88c27b125c40, msinkaut/IInkDrawingAttributes::Clone, tablet.inkdrawingattributes_clone
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
 - IInkDrawingAttributes::Clone
 - msinkaut/IInkDrawingAttributes::Clone
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
 - IInkDrawingAttributes.Clone
---

# IInkDrawingAttributes::Clone


## -description

Creates a duplicate <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

## -parameters

### -param DrawingAttributes [out, retval]

When this method returns, contains a pointer to the newly created <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object was not registered.

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

The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone">Clone</a> method is defined for the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a>, <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a>, and <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> objects. The <b>Clone</b> method returns an exact copy of the original object.

In most scenarios, the duplicate object is an exact copy of the original object, but no relation between the two objects exists. See the remarks section of this topic for details on exceptions to this.


<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object: Typically, you clone a master copy of the drawing attributes, modify one or more of the attributes, and call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes</a> method to use the modified drawing attributes.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty">Dirty Property</a>



<a href="../msinkaut/nn-msinkaut-iinkdrawingattributes.md">IInkDrawingAttributes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttribute Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes Method</a>

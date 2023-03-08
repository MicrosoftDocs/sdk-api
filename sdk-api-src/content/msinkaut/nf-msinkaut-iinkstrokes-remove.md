---
UID: NF:msinkaut.IInkStrokes.Remove
title: IInkStrokes::Remove (msinkaut.h)
description: Removes an IInkStrokeDisp object from a InkStrokes collection.
helpviewer_keywords: ["IInkStrokes interface [Tablet PC]","Remove method","IInkStrokes.Remove","IInkStrokes::Remove","Remove","Remove method [Tablet PC]","Remove method [Tablet PC]","IInkStrokes interface","ce7a7842-c7c8-4f73-8f68-05b22c2199de","msinkaut/IInkStrokes::Remove","tablet.inkstrokes_remove"]
old-location: tablet\inkstrokes_remove.htm
tech.root: tablet
ms.assetid: ce7a7842-c7c8-4f73-8f68-05b22c2199de
ms.date: 12/05/2018
ms.keywords: IInkStrokes interface [Tablet PC],Remove method, IInkStrokes.Remove, IInkStrokes::Remove, Remove, Remove method [Tablet PC], Remove method [Tablet PC],IInkStrokes interface, ce7a7842-c7c8-4f73-8f68-05b22c2199de, msinkaut/IInkStrokes::Remove, tablet.inkstrokes_remove
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
 - IInkStrokes::Remove
 - msinkaut/IInkStrokes::Remove
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
 - IInkStrokes.Remove
---

# IInkStrokes::Remove


## -description

Removes an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object from a <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param InkStroke [in]

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> to remove.

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
Cannot allocate <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> handler helper object.

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
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
IInkStroke* does not point to a valid <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and this <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object do not match.

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

<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections are sets of references to ink data and are not the actual data itself. This method removes only the collection of strokes from a snapshot of, or reference to, the data and does not remove the actual ink data. To delete the collection from the actual ink data, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a> method.

After calling the <b>Remove</b> method, the strokes in the collection are reordered. For example, after calling Strokes.Remove(Strokes.Item(0)), what used to be Strokes.Item(1) is now Strokes.Item(0), what was Strokes.Item(2) is now Strokes.Item(1), and so forth.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes">RemoveStrokes Method</a>

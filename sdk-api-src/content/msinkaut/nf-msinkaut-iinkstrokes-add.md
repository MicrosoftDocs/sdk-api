---
UID: NF:msinkaut.IInkStrokes.Add
title: IInkStrokes::Add (msinkaut.h)
description: Adds an IInkStrokeDisp object or InkStrokes collection to an existing InkStrokes collection.
helpviewer_keywords: ["5ea0932a-ba21-4c6a-a3bc-c122b5805e86","Add","Add method [Tablet PC]","Add method [Tablet PC]","IInkStrokes interface","IInkStrokes interface [Tablet PC]","Add method","IInkStrokes.Add","IInkStrokes::Add","msinkaut/IInkStrokes::Add","tablet.inkstrokes_add"]
old-location: tablet\inkstrokes_add.htm
tech.root: tablet
ms.assetid: 5ea0932a-ba21-4c6a-a3bc-c122b5805e86
ms.date: 12/05/2018
ms.keywords: 5ea0932a-ba21-4c6a-a3bc-c122b5805e86, Add, Add method [Tablet PC], Add method [Tablet PC],IInkStrokes interface, IInkStrokes interface [Tablet PC],Add method, IInkStrokes.Add, IInkStrokes::Add, msinkaut/IInkStrokes::Add, tablet.inkstrokes_add
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
 - IInkStrokes::Add
 - msinkaut/IInkStrokes::Add
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
 - IInkStrokes.Add
---

# IInkStrokes::Add


## -description

Adds an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object or <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to an existing InkStrokes collection.

## -parameters

### -param InkStroke [in]

 The stroke to add to the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

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
Cannot allocate <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> handler helper object.

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
IInkStrokeDisp* does not point to a compatible <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> being added does not match the <b>InkDisp</b> object of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  The stroke must already exist within the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, and cannot belong to another <b>InkDisp</b> object. Also, this method does not copy or otherwise alter the <b>InkDisp</b> object, but merely adds this stroke to the collection.</div>
<div> </div>
Use this method to add one stroke to an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection. To add one collection of strokes to another, use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-addstrokes">AddStrokes</a> method.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-addstrokes">AddStrokes Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>

---
UID: NF:msinkaut.IInkStrokes.AddStrokes
title: IInkStrokes::AddStrokes (msinkaut.h)
description: Adds a Strokes collection to an existing Strokes collection.
helpviewer_keywords: ["76580828-c776-4787-843c-db0acb768321","AddStrokes","AddStrokes method [Tablet PC]","AddStrokes method [Tablet PC]","IInkStrokes interface","IInkStrokes interface [Tablet PC]","AddStrokes method","IInkStrokes.AddStrokes","IInkStrokes::AddStrokes","msinkaut/IInkStrokes::AddStrokes","tablet.inkstrokes_addstrokes"]
old-location: tablet\inkstrokes_addstrokes.htm
tech.root: tablet
ms.assetid: 76580828-c776-4787-843c-db0acb768321
ms.date: 12/05/2018
ms.keywords: 76580828-c776-4787-843c-db0acb768321, AddStrokes, AddStrokes method [Tablet PC], AddStrokes method [Tablet PC],IInkStrokes interface, IInkStrokes interface [Tablet PC],AddStrokes method, IInkStrokes.AddStrokes, IInkStrokes::AddStrokes, msinkaut/IInkStrokes::AddStrokes, tablet.inkstrokes_addstrokes
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
 - IInkStrokes::AddStrokes
 - msinkaut/IInkStrokes::AddStrokes
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
 - IInkStrokes.AddStrokes
---

# IInkStrokes::AddStrokes


## -description

Adds a <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">Strokes</a> collection to an existing Strokes collection.

## -parameters

### -param InkStrokes [in]

 The collection of strokes to add to the collection of strokes.

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
IInkStrokes* does not point to a compatible <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that is being added must match the <b>InkDisp</b> object of the InkStrokes collection to which it is being added.

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

<div class="alert"><b>Note</b>  This collection must already exist within the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object and cannot belong to another <b>InkDisp</b> object. Also, this does not copy or otherwise alter the <b>InkDisp</b> object, but merely adds this collection of strokes to the collection.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add">Add Method [InkStrokes Collection]</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>

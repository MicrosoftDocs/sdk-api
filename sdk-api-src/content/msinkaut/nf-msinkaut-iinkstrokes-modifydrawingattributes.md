---
UID: NF:msinkaut.IInkStrokes.ModifyDrawingAttributes
title: IInkStrokes::ModifyDrawingAttributes (msinkaut.h)
description: Sets the drawing attributes of all of the strokes in an InkStrokes collection.
helpviewer_keywords: ["IInkStrokes interface [Tablet PC]","ModifyDrawingAttributes method","IInkStrokes.ModifyDrawingAttributes","IInkStrokes::ModifyDrawingAttributes","ModifyDrawingAttributes","ModifyDrawingAttributes method [Tablet PC]","ModifyDrawingAttributes method [Tablet PC]","IInkStrokes interface","b249edd9-dfa4-4538-9764-a4365f9df527","msinkaut/IInkStrokes::ModifyDrawingAttributes","tablet.inkstrokes_modifydrawingattributes"]
old-location: tablet\inkstrokes_modifydrawingattributes.htm
tech.root: tablet
ms.assetid: b249edd9-dfa4-4538-9764-a4365f9df527
ms.date: 12/05/2018
ms.keywords: IInkStrokes interface [Tablet PC],ModifyDrawingAttributes method, IInkStrokes.ModifyDrawingAttributes, IInkStrokes::ModifyDrawingAttributes, ModifyDrawingAttributes, ModifyDrawingAttributes method [Tablet PC], ModifyDrawingAttributes method [Tablet PC],IInkStrokes interface, b249edd9-dfa4-4538-9764-a4365f9df527, msinkaut/IInkStrokes::ModifyDrawingAttributes, tablet.inkstrokes_modifydrawingattributes
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
 - IInkStrokes::ModifyDrawingAttributes
 - msinkaut/IInkStrokes::ModifyDrawingAttributes
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
 - IInkStrokes.ModifyDrawingAttributes
---

# IInkStrokes::ModifyDrawingAttributes


## -description

Sets the drawing attributes of all of the strokes in an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param DrawAttrs [in]

The new drawing attributes for all of the strokes in the collection.

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

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>

---
UID: NF:msinkaut.IInkCustomStrokes.Add
title: IInkCustomStrokes::Add (msinkaut.h)
description: Adds an InkStrokes collection to an IInkCustomStrokes collection.
helpviewer_keywords: ["482906b2-131e-4baa-8ed7-c11f79f05e4b","Add","Add method [Tablet PC]","Add method [Tablet PC]","IInkCustomStrokes interface","IInkCustomStrokes interface [Tablet PC]","Add method","IInkCustomStrokes.Add","IInkCustomStrokes::Add","msinkaut/IInkCustomStrokes::Add","tablet.iinkcustomstrokes_add"]
old-location: tablet\iinkcustomstrokes_add.htm
tech.root: tablet
ms.assetid: 482906b2-131e-4baa-8ed7-c11f79f05e4b
ms.date: 12/05/2018
ms.keywords: 482906b2-131e-4baa-8ed7-c11f79f05e4b, Add, Add method [Tablet PC], Add method [Tablet PC],IInkCustomStrokes interface, IInkCustomStrokes interface [Tablet PC],Add method, IInkCustomStrokes.Add, IInkCustomStrokes::Add, msinkaut/IInkCustomStrokes::Add, tablet.iinkcustomstrokes_add
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
 - IInkCustomStrokes::Add
 - msinkaut/IInkCustomStrokes::Add
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
 - IInkCustomStrokes.Add
---

# IInkCustomStrokes::Add


## -description

Adds an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection.

## -parameters

### -param Name [in]

Specifies the name of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to add to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Strokes [in]

Specifies the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to add to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The item already exists in the collection or a parameter contained an invalid pointer.

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
The collection of strokes is incompatible with the API.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different INK object.

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
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
---
UID: NF:msinkaut.IInkStrokes.Item
title: IInkStrokes::Item (msinkaut.h)
description: Retrieves the IInkStrokeDisp object at the specified index within the InkStrokes collection.
helpviewer_keywords: ["IInkStrokes interface [Tablet PC]","Item method","IInkStrokes.Item","IInkStrokes::Item","Item","Item method [Tablet PC]","Item method [Tablet PC]","IInkStrokes interface","ecffbdf0-4b1c-46de-bc4c-c44812dae27a","msinkaut/IInkStrokes::Item","tablet.inkstrokes_item"]
old-location: tablet\inkstrokes_item.htm
tech.root: tablet
ms.assetid: ecffbdf0-4b1c-46de-bc4c-c44812dae27a
ms.date: 12/05/2018
ms.keywords: IInkStrokes interface [Tablet PC],Item method, IInkStrokes.Item, IInkStrokes::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkStrokes interface, ecffbdf0-4b1c-46de-bc4c-c44812dae27a, msinkaut/IInkStrokes::Item, tablet.inkstrokes_item
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
 - IInkStrokes::Item
 - msinkaut/IInkStrokes::Item
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
 - IInkStrokes.Item
---

# IInkStrokes::Item


## -description

Retrieves the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object at the specified index within the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param Index [in]

The zero-based index of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object to get.

### -param Stroke [out, retval]

When this method returns, contains a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object at the specified index within the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

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
<dt><b>CO_E_CLASSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not a valid VARIANT type.

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
Type object not registered.

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
<dt><b>TPC_E_RECOGNIZER_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The recognizers registry key is corrupted or your environment does not support handwriting recognition.




</td>
</tr>
</table>

## -remarks

An error occurs if the index doesn't match any existing member of the collection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>

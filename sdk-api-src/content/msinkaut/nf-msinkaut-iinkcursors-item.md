---
UID: NF:msinkaut.IInkCursors.Item
title: IInkCursors::Item (msinkaut.h)
description: Returns the IInkCursor object at the specified index within the IInkCursors collection.
helpviewer_keywords: ["59174954-4994-4773-acee-a3db363cb8fe","IInkCursors interface [Tablet PC]","Item method","IInkCursors.Item","IInkCursors::Item","Item","Item method [Tablet PC]","Item method [Tablet PC]","IInkCursors interface","msinkaut/IInkCursors::Item","tablet.iinkcursors_item"]
old-location: tablet\iinkcursors_item.htm
tech.root: tablet
ms.assetid: 59174954-4994-4773-acee-a3db363cb8fe
ms.date: 12/05/2018
ms.keywords: 59174954-4994-4773-acee-a3db363cb8fe, IInkCursors interface [Tablet PC],Item method, IInkCursors.Item, IInkCursors::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkCursors interface, msinkaut/IInkCursors::Item, tablet.iinkcursors_item
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
 - IInkCursors::Item
 - msinkaut/IInkCursors::Item
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
 - IInkCursors.Item
---

# IInkCursors::Item


## -description

Returns the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object at the specified index within the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection.

## -parameters

### -param Index [in]

The zero-based index of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object to get.

### -param Cursor [out, retval]

When this method returns, contains a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object at the specified index within the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection.

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
Type OBJECT not registered.

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

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors Interface</a>
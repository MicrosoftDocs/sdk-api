---
UID: NF:msinkaut15.IInkDivisionUnits.Item
title: IInkDivisionUnits::Item (msinkaut15.h)
description: Retrieves the IInkDivisionUnit object at the specified index within the IInkDivisionUnits collection.
helpviewer_keywords: ["332a9365-526e-43df-841f-20eed07762e7","IInkDivisionUnits interface [Tablet PC]","Item method","IInkDivisionUnits.Item","IInkDivisionUnits::Item","Item","Item method [Tablet PC]","Item method [Tablet PC]","IInkDivisionUnits interface","msinkaut15/IInkDivisionUnits::Item","tablet.iinkdivisionunits_item"]
old-location: tablet\iinkdivisionunits_item.htm
tech.root: tablet
ms.assetid: 332a9365-526e-43df-841f-20eed07762e7
ms.date: 12/05/2018
ms.keywords: 332a9365-526e-43df-841f-20eed07762e7, IInkDivisionUnits interface [Tablet PC],Item method, IInkDivisionUnits.Item, IInkDivisionUnits::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkDivisionUnits interface, msinkaut15/IInkDivisionUnits::Item, tablet.iinkdivisionunits_item
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivisionUnits::Item
 - msinkaut15/IInkDivisionUnits::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionUnits.Item
---

# IInkDivisionUnits::Item


## -description

Retrieves the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object at the specified index within the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection.

## -parameters

### -param Index [in]

The zero-based index of the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object to get.

### -param InkDivisionUnit [out, retval]

When this method returns, contains a pointer to the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit</a> object at the specified index within the <a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits</a> collection.

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
A parameter contains an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid value.

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

An error occurs if the index doesn't match any existing member of the collection.

## -see-also

<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit">IInkDivisionUnit Interface</a>



<a href="/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits">IInkDivisionUnits Interface</a>
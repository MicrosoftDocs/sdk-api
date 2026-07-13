---
UID: NF:ocidl.IEnumOleUndoUnits.Clone
title: IEnumOleUndoUnits::Clone (ocidl.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumOleUndoUnits.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumOleUndoUnits interface","IEnumOleUndoUnits interface [COM]","Clone method","IEnumOleUndoUnits.Clone","IEnumOleUndoUnits::Clone","_ole_ienumoleundounits_clone","com.ienumoleundounits_clone","ocidl/IEnumOleUndoUnits::Clone"]
old-location: com\ienumoleundounits_clone.htm
tech.root: com
ms.assetid: 0aed7771-0e9c-49b1-8c45-4dcf637cb04c
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumOleUndoUnits interface, IEnumOleUndoUnits interface [COM],Clone method, IEnumOleUndoUnits.Clone, IEnumOleUndoUnits::Clone, _ole_ienumoleundounits_clone, com.ienumoleundounits_clone, ocidl/IEnumOleUndoUnits::Clone
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumOleUndoUnits::Clone
 - ocidl/IEnumOleUndoUnits::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IEnumOleUndoUnits.Clone
---

# IEnumOleUndoUnits::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppEnum [out]

A pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a> interface pointer on the newly created enumerator. The caller must release this enumerator separately from the one from which it was cloned.

## -returns

This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified enumerator is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumoleundounits">IEnumOleUndoUnits</a>

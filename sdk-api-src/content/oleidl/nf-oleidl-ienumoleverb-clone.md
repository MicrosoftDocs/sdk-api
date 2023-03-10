---
UID: NF:oleidl.IEnumOLEVERB.Clone
title: IEnumOLEVERB::Clone (oleidl.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumOLEVERB.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumOLEVERB interface","IEnumOLEVERB interface [COM]","Clone method","IEnumOLEVERB.Clone","IEnumOLEVERB::Clone","_ole_ienumoleverb_clone","com.ienumoleverb_clone","oleidl/IEnumOLEVERB::Clone"]
old-location: com\ienumoleverb_clone.htm
tech.root: com
ms.assetid: b93eafa0-c9c5-4d3f-a9a0-c5ca95df5b03
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumOLEVERB interface, IEnumOLEVERB interface [COM],Clone method, IEnumOLEVERB.Clone, IEnumOLEVERB::Clone, _ole_ienumoleverb_clone, com.ienumoleverb_clone, oleidl/IEnumOLEVERB::Clone
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IEnumOLEVERB::Clone
 - oleidl/IEnumOLEVERB::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IEnumOLEVERB.Clone
---

# IEnumOLEVERB::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppenum [out]

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a> pointer variable that receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined.

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

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>

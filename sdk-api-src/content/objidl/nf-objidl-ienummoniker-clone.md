---
UID: NF:objidl.IEnumMoniker.Clone
title: IEnumMoniker::Clone (objidl.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumMoniker.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumMoniker interface","IEnumMoniker interface [COM]","Clone method","IEnumMoniker.Clone","IEnumMoniker::Clone","_ole_ienummoniker_clone","com.ienummoniker_clone","objidl/IEnumMoniker::Clone"]
old-location: com\ienummoniker_clone.htm
tech.root: com
ms.assetid: 6238e556-9ef4-42c7-95ba-12468cec6b52
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumMoniker interface, IEnumMoniker interface [COM],Clone method, IEnumMoniker.Clone, IEnumMoniker::Clone, _ole_ienummoniker_clone, com.ienummoniker_clone, objidl/IEnumMoniker::Clone
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IEnumMoniker::Clone
 - objidl/IEnumMoniker::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IEnumMoniker.Clone
---

# IEnumMoniker::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppenum [out]

Address of an <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> pointer variable that receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined.

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

<a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a>

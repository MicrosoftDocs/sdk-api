---
UID: NF:msctf.ITfPropertyStore.Clone
title: ITfPropertyStore::Clone (msctf.h)
description: ITfPropertyStore::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","ITfPropertyStore interface","ITfPropertyStore interface [Text Services Framework]","Clone method","ITfPropertyStore.Clone","ITfPropertyStore::Clone","_tsf_itfpropertystore_clone_ref","msctf/ITfPropertyStore::Clone","tsf.itfpropertystore_clone"]
old-location: tsf\itfpropertystore_clone.htm
tech.root: TSF
ms.assetid: 0f51a37f-e340-441e-a1f1-e67791b9c008
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],ITfPropertyStore interface, ITfPropertyStore interface [Text Services Framework],Clone method, ITfPropertyStore.Clone, ITfPropertyStore::Clone, _tsf_itfpropertystore_clone_ref, msctf/ITfPropertyStore::Clone, tsf.itfpropertystore_clone
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfPropertyStore::Clone
 - msctf/ITfPropertyStore::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfPropertyStore.Clone
---

# ITfPropertyStore::Clone


## -description

Creates an exact copy of the property store object.

## -parameters

### -param pPropStore [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a> interface pointer that receives the new property store object.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

This method creates a new property store object and initializes the new object so that it will operate as an exact copy of the original property store object. The new object must be completely independent of the original object.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore
      </a>
---
UID: NF:msctf.ITfPropertyStore.GetType
title: ITfPropertyStore::GetType (msctf.h)
description: ITfPropertyStore::GetType method
helpviewer_keywords: ["GetType","GetType method [Text Services Framework]","GetType method [Text Services Framework]","ITfPropertyStore interface","ITfPropertyStore interface [Text Services Framework]","GetType method","ITfPropertyStore.GetType","ITfPropertyStore::GetType","_tsf_itfpropertystore_gettype_ref","msctf/ITfPropertyStore::GetType","tsf.itfpropertystore_gettype"]
old-location: tsf\itfpropertystore_gettype.htm
tech.root: TSF
ms.assetid: e0b6b1b7-1994-4876-9f15-7e1c6a4f0e4b
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Text Services Framework], GetType method [Text Services Framework],ITfPropertyStore interface, ITfPropertyStore interface [Text Services Framework],GetType method, ITfPropertyStore.GetType, ITfPropertyStore::GetType, _tsf_itfpropertystore_gettype_ref, msctf/ITfPropertyStore::GetType, tsf.itfpropertystore_gettype
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
 - ITfPropertyStore::GetType
 - msctf/ITfPropertyStore::GetType
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
 - ITfPropertyStore.GetType
---

# ITfPropertyStore::GetType


## -description

Obtains the property identifier.

## -parameters

### -param pguid [out]

Pointer to a <b>GUID</b> value that receives the property identifier.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguid</i> is invalid.

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


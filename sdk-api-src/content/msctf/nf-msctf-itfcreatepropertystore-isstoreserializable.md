---
UID: NF:msctf.ITfCreatePropertyStore.IsStoreSerializable
title: ITfCreatePropertyStore::IsStoreSerializable (msctf.h)
description: ITfCreatePropertyStore::IsStoreSerializable method
helpviewer_keywords: ["ITfCreatePropertyStore interface [Text Services Framework]","IsStoreSerializable method","ITfCreatePropertyStore.IsStoreSerializable","ITfCreatePropertyStore::IsStoreSerializable","IsStoreSerializable","IsStoreSerializable method [Text Services Framework]","IsStoreSerializable method [Text Services Framework]","ITfCreatePropertyStore interface","_tsf_itfcreatepropertystore_isstoreserializable_ref","msctf/ITfCreatePropertyStore::IsStoreSerializable","tsf.itfcreatepropertystore_isstoreserializable"]
old-location: tsf\itfcreatepropertystore_isstoreserializable.htm
tech.root: TSF
ms.assetid: f5fdd81f-266b-4ff3-ab44-2d1c89a7aaea
ms.date: 12/05/2018
ms.keywords: ITfCreatePropertyStore interface [Text Services Framework],IsStoreSerializable method, ITfCreatePropertyStore.IsStoreSerializable, ITfCreatePropertyStore::IsStoreSerializable, IsStoreSerializable, IsStoreSerializable method [Text Services Framework], IsStoreSerializable method [Text Services Framework],ITfCreatePropertyStore interface, _tsf_itfcreatepropertystore_isstoreserializable_ref, msctf/ITfCreatePropertyStore::IsStoreSerializable, tsf.itfcreatepropertystore_isstoreserializable
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCreatePropertyStore::IsStoreSerializable
 - msctf/ITfCreatePropertyStore::IsStoreSerializable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfCreatePropertyStore.IsStoreSerializable
---

# ITfCreatePropertyStore::IsStoreSerializable


## -description

Determines if a property store can be stored as persistent data.

## -parameters

### -param guidProp [in]

Contains the type identifier of the property. For more information, see <a href="/windows/desktop/api/msctf/nf-msctf-itfpropertystore-gettype">ITfPropertyStore::GetType</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the text covered by the property store.

### -param pPropStore [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a> object.

### -param pfSerializable [out]

Pointer to a <b>BOOL</b> that receives a flag that indicates if the property store can be serialized. Receives nonzero if the property store can be serialized or zero otherwise.

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
</table>

## -see-also

[ITfCreatePropertyStore interface](nn-msctf-itfcreatepropertystore.md), [ITfPropertyStore interface](nn-msctf-itfpropertystore.md), [ITfPropertyStore::GetType](nf-msctf-itfpropertystore-gettype.md), [ITfRange interface](nn-msctf-itfrange.md)
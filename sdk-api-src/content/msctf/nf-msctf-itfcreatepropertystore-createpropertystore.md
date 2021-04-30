---
UID: NF:msctf.ITfCreatePropertyStore.CreatePropertyStore
title: ITfCreatePropertyStore::CreatePropertyStore (msctf.h)
description: ITfCreatePropertyStore::CreatePropertyStore method
helpviewer_keywords: ["CreatePropertyStore","CreatePropertyStore method [Text Services Framework]","CreatePropertyStore method [Text Services Framework]","ITfCreatePropertyStore interface","ITfCreatePropertyStore interface [Text Services Framework]","CreatePropertyStore method","ITfCreatePropertyStore.CreatePropertyStore","ITfCreatePropertyStore::CreatePropertyStore","_tsf_itfcreatepropertystore_createpropertystore_ref","msctf/ITfCreatePropertyStore::CreatePropertyStore","tsf.itfcreatepropertystore_createpropertystore"]
old-location: tsf\itfcreatepropertystore_createpropertystore.htm
tech.root: TSF
ms.assetid: 8c2e612c-31d8-4c89-97c4-3e248d7b7b28
ms.date: 12/05/2018
ms.keywords: CreatePropertyStore, CreatePropertyStore method [Text Services Framework], CreatePropertyStore method [Text Services Framework],ITfCreatePropertyStore interface, ITfCreatePropertyStore interface [Text Services Framework],CreatePropertyStore method, ITfCreatePropertyStore.CreatePropertyStore, ITfCreatePropertyStore::CreatePropertyStore, _tsf_itfcreatepropertystore_createpropertystore_ref, msctf/ITfCreatePropertyStore::CreatePropertyStore, tsf.itfcreatepropertystore_createpropertystore
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
 - ITfCreatePropertyStore::CreatePropertyStore
 - msctf/ITfCreatePropertyStore::CreatePropertyStore
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
 - ITfCreatePropertyStore.CreatePropertyStore
---

# ITfCreatePropertyStore::CreatePropertyStore


## -description

Creates a property store object from serialized property store data.

## -parameters

### -param guidProp [in]

Contains the type identifier of the property. For more information, see <a href="/windows/desktop/api/msctf/nf-msctf-itfpropertystore-gettype">ITfPropertyStore::GetType</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the text to be covered by the property store.

### -param cb [in]

Contains the size, in bytes, of the property store data contained in <i>pStream</i>.

### -param pStream [in]

Pointer to an <b>IStream</b> object that contains the property store data.

### -param ppStore [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a> interface pointer that receives the property store object created by this method.

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
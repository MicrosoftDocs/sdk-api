---
UID: NF:msctf.ITfPropertyStore.Serialize
title: ITfPropertyStore::Serialize (msctf.h)
description: ITfPropertyStore::Serialize method
helpviewer_keywords: ["ITfPropertyStore interface [Text Services Framework]","Serialize method","ITfPropertyStore.Serialize","ITfPropertyStore::Serialize","Serialize","Serialize method [Text Services Framework]","Serialize method [Text Services Framework]","ITfPropertyStore interface","_tsf_itfpropertystore_serialize_ref","msctf/ITfPropertyStore::Serialize","tsf.itfpropertystore_serialize"]
old-location: tsf\itfpropertystore_serialize.htm
tech.root: TSF
ms.assetid: b84bce22-684f-4326-9e28-0fc16b818732
ms.date: 12/05/2018
ms.keywords: ITfPropertyStore interface [Text Services Framework],Serialize method, ITfPropertyStore.Serialize, ITfPropertyStore::Serialize, Serialize, Serialize method [Text Services Framework], Serialize method [Text Services Framework],ITfPropertyStore interface, _tsf_itfpropertystore_serialize_ref, msctf/ITfPropertyStore::Serialize, tsf.itfpropertystore_serialize
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
 - ITfPropertyStore::Serialize
 - msctf/ITfPropertyStore::Serialize
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
 - ITfPropertyStore.Serialize
---

# ITfPropertyStore::Serialize


## -description

Called to write the property store data into a stream for serialization.

## -parameters

### -param pStream [in]

Pointer to an <b>IStream</b> object that the property store data is written to.

### -param pcb [out]

Pointer to a <b>ULONG</b> value that receives the number of bytes written to the stream.

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
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

The method must not move the stream insertion point before writing to the stream. The method must leave the insertion point at the end of the data written by the method.


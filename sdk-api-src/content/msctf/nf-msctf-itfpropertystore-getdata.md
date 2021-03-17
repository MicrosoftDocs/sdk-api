---
UID: NF:msctf.ITfPropertyStore.GetData
title: ITfPropertyStore::GetData (msctf.h)
description: ITfPropertyStore::GetData method
helpviewer_keywords: ["GetData","GetData method [Text Services Framework]","GetData method [Text Services Framework]","ITfPropertyStore interface","ITfPropertyStore interface [Text Services Framework]","GetData method","ITfPropertyStore.GetData","ITfPropertyStore::GetData","_tsf_itfpropertystore_getdata_ref","msctf/ITfPropertyStore::GetData","tsf.itfpropertystore_getdata"]
old-location: tsf\itfpropertystore_getdata.htm
tech.root: TSF
ms.assetid: 190506ea-4f15-4976-a337-bfd873e58aff
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Text Services Framework], GetData method [Text Services Framework],ITfPropertyStore interface, ITfPropertyStore interface [Text Services Framework],GetData method, ITfPropertyStore.GetData, ITfPropertyStore::GetData, _tsf_itfpropertystore_getdata_ref, msctf/ITfPropertyStore::GetData, tsf.itfpropertystore_getdata
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
 - ITfPropertyStore::GetData
 - msctf/ITfPropertyStore::GetData
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
 - ITfPropertyStore.GetData
---

# ITfPropertyStore::GetData


## -description

Obtains the property store data.

## -parameters

### -param pvarValue [out]

Pointer to a <b>VARIANT</b> value that receives property data.

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
<i>pvarValue</i> is invalid.

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


---
UID: NF:msctf.ITfFunctionProvider.GetType
title: ITfFunctionProvider::GetType (msctf.h)
description: ITfFunctionProvider::GetType method
helpviewer_keywords: ["GetType","GetType method [Text Services Framework]","GetType method [Text Services Framework]","ITfFunctionProvider interface","ITfFunctionProvider interface [Text Services Framework]","GetType method","ITfFunctionProvider.GetType","ITfFunctionProvider::GetType","_tsf_itffunctionprovider_gettype_ref","msctf/ITfFunctionProvider::GetType","tsf.itffunctionprovider_gettype"]
old-location: tsf\itffunctionprovider_gettype.htm
tech.root: TSF
ms.assetid: fff9ad62-f777-423c-a59d-ebd7d99da6a9
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Text Services Framework], GetType method [Text Services Framework],ITfFunctionProvider interface, ITfFunctionProvider interface [Text Services Framework],GetType method, ITfFunctionProvider.GetType, ITfFunctionProvider::GetType, _tsf_itffunctionprovider_gettype_ref, msctf/ITfFunctionProvider::GetType, tsf.itffunctionprovider_gettype
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
 - ITfFunctionProvider::GetType
 - msctf/ITfFunctionProvider::GetType
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
 - ITfFunctionProvider.GetType
---

# ITfFunctionProvider::GetType


## -description

Obtains the type identifier for the function provider.

## -parameters

### -param pguid [out]

Pointer to a GUID value that receives the type identifier of the function provider.

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
The method was successful

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
</table>


---
UID: NF:msctf.IEnumTfFunctionProviders.Clone
title: IEnumTfFunctionProviders::Clone (msctf.h)
description: IEnumTfFunctionProviders::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfFunctionProviders interface","IEnumTfFunctionProviders interface [Text Services Framework]","Clone method","IEnumTfFunctionProviders.Clone","IEnumTfFunctionProviders::Clone","_tsf_ienumtffunctionproviders_clone_ref","msctf/IEnumTfFunctionProviders::Clone","tsf.ienumtffunctionproviders_clone"]
old-location: tsf\ienumtffunctionproviders_clone.htm
tech.root: TSF
ms.assetid: fa4b8682-4f99-425d-8ae7-a510e109fe64
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfFunctionProviders interface, IEnumTfFunctionProviders interface [Text Services Framework],Clone method, IEnumTfFunctionProviders.Clone, IEnumTfFunctionProviders::Clone, _tsf_ienumtffunctionproviders_clone_ref, msctf/IEnumTfFunctionProviders::Clone, tsf.ienumtffunctionproviders_clone
f1_keywords:
- msctf/IEnumTfFunctionProviders.Clone
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- IEnumTfFunctionProviders.Clone
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfFunctionProviders::Clone

## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtffunctionproviders">IEnumTfFunctionProviders</a> interface pointer that receives the new enumerator.


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

## -see-also

[IEnumTfFunctionProviders interface](nn-msctf-ienumtffunctionproviders.md), [ITfFunctionProvider interface](nn-msctf-itffunctionprovider.md)

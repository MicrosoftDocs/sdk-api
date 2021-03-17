---
UID: NF:msctf.IEnumTfProperties.Clone
title: IEnumTfProperties::Clone (msctf.h)
description: IEnumTfProperties::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfProperties interface","IEnumTfProperties interface [Text Services Framework]","Clone method","IEnumTfProperties.Clone","IEnumTfProperties::Clone","_tsf_ienumtfproperties_clone_ref","msctf/IEnumTfProperties::Clone","tsf.ienumtfproperties_clone"]
old-location: tsf\ienumtfproperties_clone.htm
tech.root: TSF
ms.assetid: ee90f452-7e50-4b9a-b81d-b5d4244f55b4
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfProperties interface, IEnumTfProperties interface [Text Services Framework],Clone method, IEnumTfProperties.Clone, IEnumTfProperties::Clone, _tsf_ienumtfproperties_clone_ref, msctf/IEnumTfProperties::Clone, tsf.ienumtfproperties_clone
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
 - IEnumTfProperties::Clone
 - msctf/IEnumTfProperties::Clone
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
 - IEnumTfProperties.Clone
---

# IEnumTfProperties::Clone


## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfproperties">IEnumTfProperties</a> interface pointer that receives the new enumerator.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>

## -see-also

[IEnumTfProperties interface](nn-msctf-ienumtfproperties.md), [ITfProperty interface](nn-msctf-itfproperty.md)
---
UID: NF:msctf.IEnumTfFunctionProviders.Next
title: IEnumTfFunctionProviders::Next (msctf.h)
description: IEnumTfFunctionProviders::Next method
helpviewer_keywords: ["IEnumTfFunctionProviders interface [Text Services Framework]","Next method","IEnumTfFunctionProviders.Next","IEnumTfFunctionProviders::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfFunctionProviders interface","_tsf_ienumtffunctionproviders_next_ref","msctf/IEnumTfFunctionProviders::Next","tsf.ienumtffunctionproviders_next"]
old-location: tsf\ienumtffunctionproviders_next.htm
tech.root: TSF
ms.assetid: c9938eb0-c084-4663-9aef-584c987a08a7
ms.date: 12/05/2018
ms.keywords: IEnumTfFunctionProviders interface [Text Services Framework],Next method, IEnumTfFunctionProviders.Next, IEnumTfFunctionProviders::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfFunctionProviders interface, _tsf_ienumtffunctionproviders_next_ref, msctf/IEnumTfFunctionProviders::Next, tsf.ienumtffunctionproviders_next
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
 - IEnumTfFunctionProviders::Next
 - msctf/IEnumTfFunctionProviders::Next
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
 - IEnumTfFunctionProviders.Next
---

# IEnumTfFunctionProviders::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param ppCmdobj [out]

Pointer to an array of <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetch [out]

Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppCmdobj</i> is invalid.

</td>
</tr>
</table>

## -see-also

[IEnumTfFunctionProviders interface](nn-msctf-ienumtffunctionproviders.md), [ITfFunctionProvider interface](nn-msctf-itffunctionprovider.md)
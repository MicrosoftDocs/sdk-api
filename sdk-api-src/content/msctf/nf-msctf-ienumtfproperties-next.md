---
UID: NF:msctf.IEnumTfProperties.Next
title: IEnumTfProperties::Next (msctf.h)
description: IEnumTfProperties::Next method
helpviewer_keywords: ["IEnumTfProperties interface [Text Services Framework]","Next method","IEnumTfProperties.Next","IEnumTfProperties::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfProperties interface","_tsf_ienumtfproperties_next_ref","msctf/IEnumTfProperties::Next","tsf.ienumtfproperties_next"]
old-location: tsf\ienumtfproperties_next.htm
tech.root: TSF
ms.assetid: a8357166-bfc3-4740-a5b9-91c6c1825ab9
ms.date: 12/05/2018
ms.keywords: IEnumTfProperties interface [Text Services Framework],Next method, IEnumTfProperties.Next, IEnumTfProperties::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfProperties interface, _tsf_ienumtfproperties_next_ref, msctf/IEnumTfProperties::Next, tsf.ienumtfproperties_next
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
 - IEnumTfProperties::Next
 - msctf/IEnumTfProperties::Next
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
 - IEnumTfProperties.Next
---

# IEnumTfProperties::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param ppProp [out]

Pointer to an array of <a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched [out]

Pointer to a ULONG that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<i>ppProp</i> is invalid.

</td>
</tr>
</table>

## -see-also

[IEnumTfProperties interface](nn-msctf-ienumtfproperties.md), [ITfProperty interface](nn-msctf-itfproperty.md)
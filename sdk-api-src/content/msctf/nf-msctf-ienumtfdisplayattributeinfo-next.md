---
UID: NF:msctf.IEnumTfDisplayAttributeInfo.Next
title: IEnumTfDisplayAttributeInfo::Next (msctf.h)
description: IEnumTfDisplayAttributeInfo::Next method
helpviewer_keywords: ["IEnumTfDisplayAttributeInfo interface [Text Services Framework]","Next method","IEnumTfDisplayAttributeInfo.Next","IEnumTfDisplayAttributeInfo::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfDisplayAttributeInfo interface","_tsf_ienumtfdisplayattributeinfo_next_ref","msctf/IEnumTfDisplayAttributeInfo::Next","tsf.ienumtfdisplayattributeinfo_next"]
old-location: tsf\ienumtfdisplayattributeinfo_next.htm
tech.root: TSF
ms.assetid: db374ba3-8a65-4933-85cb-320c294d6041
ms.date: 12/05/2018
ms.keywords: IEnumTfDisplayAttributeInfo interface [Text Services Framework],Next method, IEnumTfDisplayAttributeInfo.Next, IEnumTfDisplayAttributeInfo::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfDisplayAttributeInfo interface, _tsf_ienumtfdisplayattributeinfo_next_ref, msctf/IEnumTfDisplayAttributeInfo::Next, tsf.ienumtfdisplayattributeinfo_next
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
 - IEnumTfDisplayAttributeInfo::Next
 - msctf/IEnumTfDisplayAttributeInfo::Next
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
 - IEnumTfDisplayAttributeInfo.Next
---

# IEnumTfDisplayAttributeInfo::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param rgInfo [out]

Pointer to an array of <a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. The number of elements can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
The method reached the end of the enumeration before the specified number of elements were obtained.

</td>
</tr>
</table>

## -see-also

[IEnumTfDisplayAttributeInfo interface](nn-msctf-ienumtfdisplayattributeinfo.md), [ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md)
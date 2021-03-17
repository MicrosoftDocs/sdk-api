---
UID: NF:msctf.IEnumTfPropertyValue.Next
title: IEnumTfPropertyValue::Next (msctf.h)
description: IEnumTfPropertyValue::Next method
helpviewer_keywords: ["IEnumTfPropertyValue interface [Text Services Framework]","Next method","IEnumTfPropertyValue.Next","IEnumTfPropertyValue::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfPropertyValue interface","_tsf_ienumtfpropertyvalue_next_ref","msctf/IEnumTfPropertyValue::Next","tsf.ienumtfpropertyvalue_next"]
old-location: tsf\ienumtfpropertyvalue_next.htm
tech.root: TSF
ms.assetid: b0fe154c-df33-443d-95a2-f41e7b02def8
ms.date: 12/05/2018
ms.keywords: IEnumTfPropertyValue interface [Text Services Framework],Next method, IEnumTfPropertyValue.Next, IEnumTfPropertyValue::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfPropertyValue interface, _tsf_ienumtfpropertyvalue_next_ref, msctf/IEnumTfPropertyValue::Next, tsf.ienumtfpropertyvalue_next
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
 - IEnumTfPropertyValue::Next
 - msctf/IEnumTfPropertyValue::Next
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
 - IEnumTfPropertyValue.Next
---

# IEnumTfPropertyValue::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param rgValues [out]

Pointer to an array of <a href="/windows/desktop/api/msctf/ns-msctf-tf_propertyval">TF_PROPERTYVAL</a> structures that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<i>rgValues</i> is invalid.

</td>
</tr>
</table>

## -see-also

[IEnumTfPropertyValue interface](nn-msctf-ienumtfpropertyvalue.md), [TF_PROPERTYVAL structure](ns-msctf-tf_propertyval.md)
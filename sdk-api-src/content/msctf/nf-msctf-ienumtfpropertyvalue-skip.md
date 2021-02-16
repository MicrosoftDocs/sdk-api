---
UID: NF:msctf.IEnumTfPropertyValue.Skip
title: IEnumTfPropertyValue::Skip (msctf.h)
description: IEnumTfPropertyValue::Skip method
helpviewer_keywords: ["IEnumTfPropertyValue interface [Text Services Framework]","Skip method","IEnumTfPropertyValue.Skip","IEnumTfPropertyValue::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfPropertyValue interface","_tsf_ienumtfpropertyvalue_skip_ref","msctf/IEnumTfPropertyValue::Skip","tsf.ienumtfpropertyvalue_skip"]
old-location: tsf\ienumtfpropertyvalue_skip.htm
tech.root: TSF
ms.assetid: 6bc11b63-c8d8-453d-b667-8a087b24cf47
ms.date: 12/05/2018
ms.keywords: IEnumTfPropertyValue interface [Text Services Framework],Skip method, IEnumTfPropertyValue.Skip, IEnumTfPropertyValue::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfPropertyValue interface, _tsf_ienumtfpropertyvalue_skip_ref, msctf/IEnumTfPropertyValue::Skip, tsf.ienumtfpropertyvalue_skip
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
 - IEnumTfPropertyValue::Skip
 - msctf/IEnumTfPropertyValue::Skip
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
 - IEnumTfPropertyValue.Skip
---

# IEnumTfPropertyValue::Skip


## -description

Moves the current position forward in the enumeration sequence by the specified number of elements.

## -parameters

### -param ulCount [in]

Contains the number of elements to skip.

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
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>

## -see-also

[IEnumTfPropertyValue interface](nn-msctf-ienumtfpropertyvalue.md), [TF_PROPERTYVAL structure](ns-msctf-tf_propertyval.md)


---
UID: NF:msctf.IEnumTfDisplayAttributeInfo.Skip
title: IEnumTfDisplayAttributeInfo::Skip (msctf.h)
description: IEnumTfDisplayAttributeInfo::Skip method
helpviewer_keywords: ["IEnumTfDisplayAttributeInfo interface [Text Services Framework]","Skip method","IEnumTfDisplayAttributeInfo.Skip","IEnumTfDisplayAttributeInfo::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfDisplayAttributeInfo interface","_tsf_ienumtfdisplayattributeinfo_skip_ref","msctf/IEnumTfDisplayAttributeInfo::Skip","tsf.ienumtfdisplayattributeinfo_skip"]
old-location: tsf\ienumtfdisplayattributeinfo_skip.htm
tech.root: TSF
ms.assetid: 5c4c9ca9-a813-406f-a507-16ccb0ff2a2a
ms.date: 12/05/2018
ms.keywords: IEnumTfDisplayAttributeInfo interface [Text Services Framework],Skip method, IEnumTfDisplayAttributeInfo.Skip, IEnumTfDisplayAttributeInfo::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfDisplayAttributeInfo interface, _tsf_ienumtfdisplayattributeinfo_skip_ref, msctf/IEnumTfDisplayAttributeInfo::Skip, tsf.ienumtfdisplayattributeinfo_skip
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
 - IEnumTfDisplayAttributeInfo::Skip
 - msctf/IEnumTfDisplayAttributeInfo::Skip
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
 - IEnumTfDisplayAttributeInfo.Skip
---

# IEnumTfDisplayAttributeInfo::Skip


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

[IEnumTfDisplayAttributeInfo interface](nn-msctf-ienumtfdisplayattributeinfo.md), [ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md)


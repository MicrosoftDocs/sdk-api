---
UID: NF:msctf.IEnumTfDisplayAttributeInfo.Clone
title: IEnumTfDisplayAttributeInfo::Clone (msctf.h)
description: IEnumTfDisplayAttributeInfo::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfDisplayAttributeInfo interface","IEnumTfDisplayAttributeInfo interface [Text Services Framework]","Clone method","IEnumTfDisplayAttributeInfo.Clone","IEnumTfDisplayAttributeInfo::Clone","_tsf_ienumtfdisplayattributeinfo_clone_ref","msctf/IEnumTfDisplayAttributeInfo::Clone","tsf.ienumtfdisplayattributeinfo_clone"]
old-location: tsf\ienumtfdisplayattributeinfo_clone.htm
tech.root: TSF
ms.assetid: 3cf57360-b07b-4a6c-850a-10c44895108d
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfDisplayAttributeInfo interface, IEnumTfDisplayAttributeInfo interface [Text Services Framework],Clone method, IEnumTfDisplayAttributeInfo.Clone, IEnumTfDisplayAttributeInfo::Clone, _tsf_ienumtfdisplayattributeinfo_clone_ref, msctf/IEnumTfDisplayAttributeInfo::Clone, tsf.ienumtfdisplayattributeinfo_clone
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
 - IEnumTfDisplayAttributeInfo::Clone
 - msctf/IEnumTfDisplayAttributeInfo::Clone
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
 - IEnumTfDisplayAttributeInfo.Clone
---

# IEnumTfDisplayAttributeInfo::Clone


## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfdisplayattributeinfo">IEnumTfDisplayAttributeInfo</a> interface pointer that receives the new enumerator.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>

## -see-also
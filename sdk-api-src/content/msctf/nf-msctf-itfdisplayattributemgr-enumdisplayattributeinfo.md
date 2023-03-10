---
UID: NF:msctf.ITfDisplayAttributeMgr.EnumDisplayAttributeInfo
title: ITfDisplayAttributeMgr::EnumDisplayAttributeInfo (msctf.h)
description: ITfDisplayAttributeMgr::EnumDisplayAttributeInfo method
helpviewer_keywords: ["EnumDisplayAttributeInfo","EnumDisplayAttributeInfo method [Text Services Framework]","EnumDisplayAttributeInfo method [Text Services Framework]","ITfDisplayAttributeMgr interface","ITfDisplayAttributeMgr interface [Text Services Framework]","EnumDisplayAttributeInfo method","ITfDisplayAttributeMgr.EnumDisplayAttributeInfo","ITfDisplayAttributeMgr::EnumDisplayAttributeInfo","_tsf_itfdisplayattributemgr_enumdisplayattributeinfo_ref","msctf/ITfDisplayAttributeMgr::EnumDisplayAttributeInfo","tsf.itfdisplayattributemgr_enumdisplayattributeinfo"]
old-location: tsf\itfdisplayattributemgr_enumdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: ea0cb5b1-46a3-43c6-a109-1972d3fcbc18
ms.date: 12/05/2018
ms.keywords: EnumDisplayAttributeInfo, EnumDisplayAttributeInfo method [Text Services Framework], EnumDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeMgr interface, ITfDisplayAttributeMgr interface [Text Services Framework],EnumDisplayAttributeInfo method, ITfDisplayAttributeMgr.EnumDisplayAttributeInfo, ITfDisplayAttributeMgr::EnumDisplayAttributeInfo, _tsf_itfdisplayattributemgr_enumdisplayattributeinfo_ref, msctf/ITfDisplayAttributeMgr::EnumDisplayAttributeInfo, tsf.itfdisplayattributemgr_enumdisplayattributeinfo
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
 - ITfDisplayAttributeMgr::EnumDisplayAttributeInfo
 - msctf/ITfDisplayAttributeMgr::EnumDisplayAttributeInfo
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
 - ITfDisplayAttributeMgr.EnumDisplayAttributeInfo
---

# ITfDisplayAttributeMgr::EnumDisplayAttributeInfo


## -description

Obtains a display attribute enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfdisplayattributeinfo">IEnumTfDisplayAttributeInfo</a> interface pointer that receives the enumerator object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumerator object cannot be initialized.

</td>
</tr>
</table>

## -see-also

[ITfDisplayAttributeMgr interface](nn-msctf-itfdisplayattributemgr.md), [IEnumTfDisplayAttributeInfo interface](nn-msctf-ienumtfdisplayattributeinfo.md)
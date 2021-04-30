---
UID: NF:msctf.ITfDisplayAttributeInfo.GetDescription
title: ITfDisplayAttributeInfo::GetDescription (msctf.h)
description: ITfDisplayAttributeInfo::GetDescription method
helpviewer_keywords: ["GetDescription","GetDescription method [Text Services Framework]","GetDescription method [Text Services Framework]","ITfDisplayAttributeInfo interface","ITfDisplayAttributeInfo interface [Text Services Framework]","GetDescription method","ITfDisplayAttributeInfo.GetDescription","ITfDisplayAttributeInfo::GetDescription","_tsf_itfdisplayattributeinfo_getdescription_ref","msctf/ITfDisplayAttributeInfo::GetDescription","tsf.itfdisplayattributeinfo_getdescription"]
old-location: tsf\itfdisplayattributeinfo_getdescription.htm
tech.root: TSF
ms.assetid: e65aedac-284d-4e2a-b574-fc469f66e06e
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Text Services Framework], GetDescription method [Text Services Framework],ITfDisplayAttributeInfo interface, ITfDisplayAttributeInfo interface [Text Services Framework],GetDescription method, ITfDisplayAttributeInfo.GetDescription, ITfDisplayAttributeInfo::GetDescription, _tsf_itfdisplayattributeinfo_getdescription_ref, msctf/ITfDisplayAttributeInfo::GetDescription, tsf.itfdisplayattributeinfo_getdescription
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
 - ITfDisplayAttributeInfo::GetDescription
 - msctf/ITfDisplayAttributeInfo::GetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfDisplayAttributeInfo.GetDescription
---

# ITfDisplayAttributeInfo::GetDescription


## -description

Obtains the description string of the display attribute.

## -parameters

### -param pbstrDesc [out]

Pointer to a BSTR value that receives the description string. This value must be allocated using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The caller must free this memory using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

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
<i>pbstrDesc</i> is invalid.

</td>
</tr>
</table>

## -see-also

[ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md), [SysAllocString function](../oleauto/nf-oleauto-sysallocstring.md), [SysFreeString function](../oleauto/nf-oleauto-sysfreestring.md)
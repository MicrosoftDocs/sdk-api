---
UID: NF:msctf.ITfDisplayAttributeInfo.GetGUID
title: ITfDisplayAttributeInfo::GetGUID (msctf.h)
description: ITfDisplayAttributeInfo::GetGUID method
helpviewer_keywords: ["GetGUID","GetGUID method [Text Services Framework]","GetGUID method [Text Services Framework]","ITfDisplayAttributeInfo interface","ITfDisplayAttributeInfo interface [Text Services Framework]","GetGUID method","ITfDisplayAttributeInfo.GetGUID","ITfDisplayAttributeInfo::GetGUID","_tsf_itfdisplayattributeinfo_getguid_ref","msctf/ITfDisplayAttributeInfo::GetGUID","tsf.itfdisplayattributeinfo_getguid"]
old-location: tsf\itfdisplayattributeinfo_getguid.htm
tech.root: TSF
ms.assetid: 5202bf19-ae24-44f4-98f0-1f9d64d383a6
ms.date: 12/05/2018
ms.keywords: GetGUID, GetGUID method [Text Services Framework], GetGUID method [Text Services Framework],ITfDisplayAttributeInfo interface, ITfDisplayAttributeInfo interface [Text Services Framework],GetGUID method, ITfDisplayAttributeInfo.GetGUID, ITfDisplayAttributeInfo::GetGUID, _tsf_itfdisplayattributeinfo_getguid_ref, msctf/ITfDisplayAttributeInfo::GetGUID, tsf.itfdisplayattributeinfo_getguid
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
 - ITfDisplayAttributeInfo::GetGUID
 - msctf/ITfDisplayAttributeInfo::GetGUID
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
 - ITfDisplayAttributeInfo.GetGUID
---

# ITfDisplayAttributeInfo::GetGUID


## -description

Obtains the GUID for the display attribute.

## -parameters

### -param pguid [out]

Pointer to a GUID value that receives the GUID for the display attribute.

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
<i>pguid</i> is invalid.

</td>
</tr>
</table>

## -see-also

[ITfDisplayAttributeInfo interface](nn-msctf-itfdisplayattributeinfo.md)


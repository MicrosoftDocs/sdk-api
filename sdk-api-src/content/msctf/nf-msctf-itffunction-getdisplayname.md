---
UID: NF:msctf.ITfFunction.GetDisplayName
title: ITfFunction::GetDisplayName (msctf.h)
description: ITfFunction::GetDisplayName method
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [Text Services Framework]","GetDisplayName method [Text Services Framework]","ITfFunction interface","ITfFunction interface [Text Services Framework]","GetDisplayName method","ITfFunction.GetDisplayName","ITfFunction::GetDisplayName","_tsf_itffunction_getdisplayname_ref","msctf/ITfFunction::GetDisplayName","tsf.itffunction_getdisplayname"]
old-location: tsf\itffunction_getdisplayname.htm
tech.root: TSF
ms.assetid: da52ca6d-9606-45c5-8db9-c876c827df14
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Text Services Framework], GetDisplayName method [Text Services Framework],ITfFunction interface, ITfFunction interface [Text Services Framework],GetDisplayName method, ITfFunction.GetDisplayName, ITfFunction::GetDisplayName, _tsf_itffunction_getdisplayname_ref, msctf/ITfFunction::GetDisplayName, tsf.itffunction_getdisplayname
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
 - ITfFunction::GetDisplayName
 - msctf/ITfFunction::GetDisplayName
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
 - ITfFunction.GetDisplayName
---

# ITfFunction::GetDisplayName


## -description

Obtains the function display name.

## -parameters

### -param pbstrName [out]

Pointer to a BSTR value that receives the display name. This value must be allocated using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The caller must free this memory using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstrName</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
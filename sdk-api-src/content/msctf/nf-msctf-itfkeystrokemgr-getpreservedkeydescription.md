---
UID: NF:msctf.ITfKeystrokeMgr.GetPreservedKeyDescription
title: ITfKeystrokeMgr::GetPreservedKeyDescription (msctf.h)
description: ITfKeystrokeMgr::GetPreservedKeyDescription method
helpviewer_keywords: ["GetPreservedKeyDescription","GetPreservedKeyDescription method [Text Services Framework]","GetPreservedKeyDescription method [Text Services Framework]","ITfKeystrokeMgr interface","ITfKeystrokeMgr interface [Text Services Framework]","GetPreservedKeyDescription method","ITfKeystrokeMgr.GetPreservedKeyDescription","ITfKeystrokeMgr::GetPreservedKeyDescription","_tsf_itfkeystrokemgr_getpreservedkeydescription_ref","msctf/ITfKeystrokeMgr::GetPreservedKeyDescription","tsf.itfkeystrokemgr_getpreservedkeydescription"]
old-location: tsf\itfkeystrokemgr_getpreservedkeydescription.htm
tech.root: TSF
ms.assetid: 5ae2b56f-0dd9-4f37-a677-20b53c7200c7
ms.date: 12/05/2018
ms.keywords: GetPreservedKeyDescription, GetPreservedKeyDescription method [Text Services Framework], GetPreservedKeyDescription method [Text Services Framework],ITfKeystrokeMgr interface, ITfKeystrokeMgr interface [Text Services Framework],GetPreservedKeyDescription method, ITfKeystrokeMgr.GetPreservedKeyDescription, ITfKeystrokeMgr::GetPreservedKeyDescription, _tsf_itfkeystrokemgr_getpreservedkeydescription_ref, msctf/ITfKeystrokeMgr::GetPreservedKeyDescription, tsf.itfkeystrokemgr_getpreservedkeydescription
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
 - ITfKeystrokeMgr::GetPreservedKeyDescription
 - msctf/ITfKeystrokeMgr::GetPreservedKeyDescription
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
 - ITfKeystrokeMgr.GetPreservedKeyDescription
---

# ITfKeystrokeMgr::GetPreservedKeyDescription


## -description

Obtains the description string of an existing preserved key.

## -parameters

### -param rguid [in]

Contains the command GUID of the preserved key.

### -param pbstrDesc [out]

Pointer to a BSTR value the receives the description string. The caller must free this memory using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

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
One or more parameters is invalid or the preserved key is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

Preserved keys are registered by TSF text services and provide keyboard shortcuts to common commands implemented by the TSF text service.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfkeystrokemgr">ITfKeystrokeMgr</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
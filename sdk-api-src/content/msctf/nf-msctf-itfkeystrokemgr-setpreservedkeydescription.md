---
UID: NF:msctf.ITfKeystrokeMgr.SetPreservedKeyDescription
title: ITfKeystrokeMgr::SetPreservedKeyDescription (msctf.h)
description: ITfKeystrokeMgr::SetPreservedKeyDescription method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","SetPreservedKeyDescription method","ITfKeystrokeMgr.SetPreservedKeyDescription","ITfKeystrokeMgr::SetPreservedKeyDescription","SetPreservedKeyDescription","SetPreservedKeyDescription method [Text Services Framework]","SetPreservedKeyDescription method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_setpreservedkeydescription_ref","msctf/ITfKeystrokeMgr::SetPreservedKeyDescription","tsf.itfkeystrokemgr_setpreservedkeydescription"]
old-location: tsf\itfkeystrokemgr_setpreservedkeydescription.htm
tech.root: TSF
ms.assetid: feb83f22-652c-4fec-b35d-a0cc41eab533
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],SetPreservedKeyDescription method, ITfKeystrokeMgr.SetPreservedKeyDescription, ITfKeystrokeMgr::SetPreservedKeyDescription, SetPreservedKeyDescription, SetPreservedKeyDescription method [Text Services Framework], SetPreservedKeyDescription method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_setpreservedkeydescription_ref, msctf/ITfKeystrokeMgr::SetPreservedKeyDescription, tsf.itfkeystrokemgr_setpreservedkeydescription
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
 - ITfKeystrokeMgr::SetPreservedKeyDescription
 - msctf/ITfKeystrokeMgr::SetPreservedKeyDescription
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
 - ITfKeystrokeMgr.SetPreservedKeyDescription
---

# ITfKeystrokeMgr::SetPreservedKeyDescription


## -description

Modifies the description string of an existing preserved key.

## -parameters

### -param rguid [in]

Contains the command GUID of the preserved key.

### -param pchDesc [in]

Pointer to a Unicode string that contains the new description of the preserved key. This cannot be <b>NULL</b> unless <i>cchDesc</i> is zero.

### -param cchDesc [in]

Number of characters in <i>pchDesc</i>. Pass zero for this parameter if no description is required.

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
One or more parameters are invalid or the preserved key is not found.

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



<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-getpreservedkeydescription">ITfKeystrokeMgr::GetPreservedKeyDescription
      </a>
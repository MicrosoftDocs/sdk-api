---
UID: NF:msctf.ITfKeystrokeMgr.IsPreservedKey
title: ITfKeystrokeMgr::IsPreservedKey (msctf.h)
description: ITfKeystrokeMgr::IsPreservedKey method
helpviewer_keywords: ["ITfKeystrokeMgr interface [Text Services Framework]","IsPreservedKey method","ITfKeystrokeMgr.IsPreservedKey","ITfKeystrokeMgr::IsPreservedKey","IsPreservedKey","IsPreservedKey method [Text Services Framework]","IsPreservedKey method [Text Services Framework]","ITfKeystrokeMgr interface","_tsf_itfkeystrokemgr_ispreservedkey_ref","msctf/ITfKeystrokeMgr::IsPreservedKey","tsf.itfkeystrokemgr_ispreservedkey"]
old-location: tsf\itfkeystrokemgr_ispreservedkey.htm
tech.root: TSF
ms.assetid: 50deac9c-b659-494b-9cda-d6109fa39363
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr interface [Text Services Framework],IsPreservedKey method, ITfKeystrokeMgr.IsPreservedKey, ITfKeystrokeMgr::IsPreservedKey, IsPreservedKey, IsPreservedKey method [Text Services Framework], IsPreservedKey method [Text Services Framework],ITfKeystrokeMgr interface, _tsf_itfkeystrokemgr_ispreservedkey_ref, msctf/ITfKeystrokeMgr::IsPreservedKey, tsf.itfkeystrokemgr_ispreservedkey
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
 - ITfKeystrokeMgr::IsPreservedKey
 - msctf/ITfKeystrokeMgr::IsPreservedKey
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
 - ITfKeystrokeMgr.IsPreservedKey
---

# ITfKeystrokeMgr::IsPreservedKey


## -description

Determines if a command GUID and key combination is a preserved key.

## -parameters

### -param rguid [in]

Specifies the command GUID of the preserved key. This is the GUID passed in the text service call to <a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-preservekey">ITfKeystrokeMgr::PreserveKey</a>.

### -param pprekey [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY</a> structure that identifies the preserved key. The <b>uVKey</b> member contains the virtual key code and the <b>uModifiers</b> member identifies the modifiers of the preserved key. The <b>uVKey</b> member must be less than 256.

### -param pfRegistered [out]

Pointer to a BOOL that receives <b>TRUE</b> if the command GUID and key combination is a registered preserved key, or <b>FALSE</b> otherwise.

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
The method was successful and the preserved key was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was successful, but the preserved key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

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



<a href="/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-preservekey">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_preservedkey">TF_PRESERVEDKEY
      </a>
---
UID: NF:msctf.ITfInputProcessorProfileMgr.GetActiveProfile
title: ITfInputProcessorProfileMgr::GetActiveProfile (msctf.h)
description: This method returns the current active profile.
helpviewer_keywords: ["GetActiveProfile","GetActiveProfile method [Text Services Framework]","GetActiveProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","ITfInputProcessorProfileMgr interface [Text Services Framework]","GetActiveProfile method","ITfInputProcessorProfileMgr.GetActiveProfile","ITfInputProcessorProfileMgr::GetActiveProfile","msctf/ITfInputProcessorProfileMgr::GetActiveProfile","tsf.itfinputprocessorprofilemgr_getactiveprofile"]
old-location: tsf\itfinputprocessorprofilemgr_getactiveprofile.htm
tech.root: TSF
ms.assetid: 4fd03327-c0c4-4dd6-b68a-8faae48c9a3d
ms.date: 12/05/2018
ms.keywords: GetActiveProfile, GetActiveProfile method [Text Services Framework], GetActiveProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, ITfInputProcessorProfileMgr interface [Text Services Framework],GetActiveProfile method, ITfInputProcessorProfileMgr.GetActiveProfile, ITfInputProcessorProfileMgr::GetActiveProfile, msctf/ITfInputProcessorProfileMgr::GetActiveProfile, tsf.itfinputprocessorprofilemgr_getactiveprofile
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileMgr::GetActiveProfile
 - msctf/ITfInputProcessorProfileMgr::GetActiveProfile
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
 - ITfInputProcessorProfileMgr.GetActiveProfile
---

# ITfInputProcessorProfileMgr::GetActiveProfile


## -description

This method returns the current active profile.

## -parameters

### -param catid [in]

[in] The category id for the profile. This must be GUID_TFCAT_TIP_KEYBOARD. Only GUID_TFCAT_TIP_KEYBOARD is supported.

### -param pProfile [out]

[out] The buffer to receive the profile information.

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
The profile was not found or is not active.

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
</table>


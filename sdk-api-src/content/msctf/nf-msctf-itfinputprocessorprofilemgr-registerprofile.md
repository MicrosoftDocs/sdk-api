---
UID: NF:msctf.ITfInputProcessorProfileMgr.RegisterProfile
title: ITfInputProcessorProfileMgr::RegisterProfile (msctf.h)
description: The ITfInputProcessorProfileMgr::RegisterProfile method registers the text service and the profile.
helpviewer_keywords: ["ITfInputProcessorProfileMgr interface [Text Services Framework]","RegisterProfile method","ITfInputProcessorProfileMgr.RegisterProfile","ITfInputProcessorProfileMgr::RegisterProfile","RegisterProfile","RegisterProfile method [Text Services Framework]","RegisterProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","TF_RP_HIDDENINSETTINGUI","TF_RP_LOCALPROCESS","TF_RP_LOCALTHREAD","msctf/ITfInputProcessorProfileMgr::RegisterProfile","tsf.itfinputprocessorprofilemgr_registerprofile"]
old-location: tsf\itfinputprocessorprofilemgr_registerprofile.htm
tech.root: TSF
ms.assetid: b497409d-96b8-41d1-9512-5d79494c6287
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileMgr interface [Text Services Framework],RegisterProfile method, ITfInputProcessorProfileMgr.RegisterProfile, ITfInputProcessorProfileMgr::RegisterProfile, RegisterProfile, RegisterProfile method [Text Services Framework], RegisterProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, TF_RP_HIDDENINSETTINGUI, TF_RP_LOCALPROCESS, TF_RP_LOCALTHREAD, msctf/ITfInputProcessorProfileMgr::RegisterProfile, tsf.itfinputprocessorprofilemgr_registerprofile
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
 - ITfInputProcessorProfileMgr::RegisterProfile
 - msctf/ITfInputProcessorProfileMgr::RegisterProfile
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
 - ITfInputProcessorProfileMgr.RegisterProfile
---

# ITfInputProcessorProfileMgr::RegisterProfile


## -description

The <b>ITfInputProcessorProfileMgr::RegisterProfile</b> method registers the text service and the profile.

## -parameters

### -param rclsid [in]

[in] CLSID of the text service.

### -param langid [in]

[in] The language id of the profile.

### -param guidProfile [in]

[in] The GUID to identify the profile.

### -param pchDesc

[in, size_is(cchDesc)] The description of the profile.

### -param cchDesc [in]

[in] The length of pchDesc.

### -param pchIconFile

[in, size_is(cchFile] The full path of the icon file.

### -param cchFile [in]

[in] The length of pchIconFile.

### -param uIconIndex [in]

[in] The icon index of the icon file for this profile.

### -param hklsubstitute [in]

[in] The substitute hkl of this profile.

### -param dwPreferredLayout [in]

[in] Unused. this must be 0.

### -param bEnabledByDefault [in]

[in] True if this profile is enabled by default.

### -param dwFlags [in]

[in] The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RP_HIDDENINSETTINGUI"></a><a id="tf_rp_hiddeninsettingui"></a><dl>
<dt><b>TF_RP_HIDDENINSETTINGUI</b></dt>
</dl>
</td>
<td width="60%">
This profile will not appear in the setting UI.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RP_LOCALPROCESS"></a><a id="tf_rp_localprocess"></a><dl>
<dt><b>TF_RP_LOCALPROCESS</b></dt>
</dl>
</td>
<td width="60%">
This profile is available only on the local process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_RP_LOCALTHREAD"></a><a id="tf_rp_localthread"></a><dl>
<dt><b>TF_RP_LOCALTHREAD</b></dt>
</dl>
</td>
<td width="60%">
This profile is available only on the local thread.

</td>
</tr>
</table>

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


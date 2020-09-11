---
UID: NF:msctf.ITfInputProcessorProfileMgr.UnregisterProfile
title: ITfInputProcessorProfileMgr::UnregisterProfile (msctf.h)
description: The ITfInputProcessorProfileMgr::UnregisterProfile method unregisters the text service and the profile.
helpviewer_keywords: ["ITfInputProcessorProfileMgr interface [Text Services Framework]","UnregisterProfile method","ITfInputProcessorProfileMgr.UnregisterProfile","ITfInputProcessorProfileMgr::UnregisterProfile","TF_URP_ALLPROFILES","TF_URP_LOCALPROCESS","TF_URP_LOCALTHREAD","UnregisterProfile","UnregisterProfile method [Text Services Framework]","UnregisterProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","msctf/ITfInputProcessorProfileMgr::UnregisterProfile","tsf.itfinputprocessorprofilemgr_unregisterprofile"]
old-location: tsf\itfinputprocessorprofilemgr_unregisterprofile.htm
tech.root: TSF
ms.assetid: 7b05beea-991a-406f-a08d-28cdd87c9d7d
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileMgr interface [Text Services Framework],UnregisterProfile method, ITfInputProcessorProfileMgr.UnregisterProfile, ITfInputProcessorProfileMgr::UnregisterProfile, TF_URP_ALLPROFILES, TF_URP_LOCALPROCESS, TF_URP_LOCALTHREAD, UnregisterProfile, UnregisterProfile method [Text Services Framework], UnregisterProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, msctf/ITfInputProcessorProfileMgr::UnregisterProfile, tsf.itfinputprocessorprofilemgr_unregisterprofile
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
 - ITfInputProcessorProfileMgr::UnregisterProfile
 - msctf/ITfInputProcessorProfileMgr::UnregisterProfile
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
 - ITfInputProcessorProfileMgr.UnregisterProfile
---

# ITfInputProcessorProfileMgr::UnregisterProfile


## -description

The <b>ITfInputProcessorProfileMgr::UnregisterProfile</b> method unregisters the text service and the profile.

## -parameters

### -param rclsid [in]

[in] CLSID of the text service.

### -param langid [in]

[in] The language id of the profile.

### -param guidProfile [in]

[in] The GUID to identify the profile.

### -param dwFlags [in]

[in] The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_URP_ALLPROFILES"></a><a id="tf_urp_allprofiles"></a><dl>
<dt><b>TF_URP_ALLPROFILES</b></dt>
</dl>
</td>
<td width="60%">
If this bit is on, <b>UnregistrProfile</b> unregisters all profiles of the <i>rclsid</i> parameter. The <i>langid</i> and <i>guidProfile</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_URP_LOCALPROCESS"></a><a id="tf_urp_localprocess"></a><dl>
<dt><b>TF_URP_LOCALPROCESS</b></dt>
</dl>
</td>
<td width="60%">
The profile was registered on the local process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_URP_LOCALTHREAD"></a><a id="tf_urp_localthread"></a><dl>
<dt><b>TF_URP_LOCALTHREAD</b></dt>
</dl>
</td>
<td width="60%">
The profile was registered on the local thread.

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


---
UID: NF:msctf.ITfInputProcessorProfileMgr.DeactivateProfile
title: ITfInputProcessorProfileMgr::DeactivateProfile (msctf.h)
description: The ITfInputProcessorProfileMgr::DeactivateProfile method deactivates the specified text service's profile or keyboard layout.
helpviewer_keywords: ["DeactivateProfile","DeactivateProfile method [Text Services Framework]","DeactivateProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","ITfInputProcessorProfileMgr interface [Text Services Framework]","DeactivateProfile method","ITfInputProcessorProfileMgr.DeactivateProfile","ITfInputProcessorProfileMgr::DeactivateProfile","TF_IPPMF_DISABLEPROFILE","TF_IPPMF_FORPROCESS","TF_IPPMF_FORSESSION","TF_PROFILETYPE_INPUTPROCESSOR","TF_PROFILETYPE_KEYBOARDLAYOUT","msctf/ITfInputProcessorProfileMgr::DeactivateProfile","tsf.itfinputprocessorprofilemgr_deactivateprofile"]
old-location: tsf\itfinputprocessorprofilemgr_deactivateprofile.htm
tech.root: TSF
ms.assetid: 8d2bd329-1b17-4b03-8c75-74d99ccc0f08
ms.date: 12/05/2018
ms.keywords: DeactivateProfile, DeactivateProfile method [Text Services Framework], DeactivateProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, ITfInputProcessorProfileMgr interface [Text Services Framework],DeactivateProfile method, ITfInputProcessorProfileMgr.DeactivateProfile, ITfInputProcessorProfileMgr::DeactivateProfile, TF_IPPMF_DISABLEPROFILE, TF_IPPMF_FORPROCESS, TF_IPPMF_FORSESSION, TF_PROFILETYPE_INPUTPROCESSOR, TF_PROFILETYPE_KEYBOARDLAYOUT, msctf/ITfInputProcessorProfileMgr::DeactivateProfile, tsf.itfinputprocessorprofilemgr_deactivateprofile
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
 - ITfInputProcessorProfileMgr::DeactivateProfile
 - msctf/ITfInputProcessorProfileMgr::DeactivateProfile
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
 - ITfInputProcessorProfileMgr.DeactivateProfile
---

# ITfInputProcessorProfileMgr::DeactivateProfile


## -description

The <b>ITfInputProcessorProfileMgr::DeactivateProfile</b> method deactivates the specified text service's profile or keyboard layout.

## -parameters

### -param dwProfileType [in]

[in] The type of this profile. This is one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_INPUTPROCESSOR"></a><a id="tf_profiletype_inputprocessor"></a><dl>
<dt><b>TF_PROFILETYPE_INPUTPROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
This is a text service.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_KEYBOARDLAYOUT"></a><a id="tf_profiletype_keyboardlayout"></a><dl>
<dt><b>TF_PROFILETYPE_KEYBOARDLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
This is a keyboard layout.

</td>
</tr>
</table>

### -param langid [in]

[in] The language id of the profile to be activated.

### -param clsid [in]

[in] The CLSID of the text service of the profile to be activated. This must be CLSID_NULL if <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT.

### -param guidProfile [in]

[in] The guidProfile of the profile to be activated. This must be GUID_NULL if <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT.

### -param hkl [in]

[in] The handle of the keyboard layout. This must be <b>NULL</b> if <i>dwProfileType</i> is TF_PROFILETYPE_INPUTPROCESSOR.

### -param dwFlags [in]

The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_FORPROCESS"></a><a id="tf_ippmf_forprocess"></a><dl>
<dt><b>TF_IPPMF_FORPROCESS</b></dt>
</dl>
</td>
<td width="60%">
Deactivate this profile for all threads in the process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_FORSESSION"></a><a id="tf_ippmf_forsession"></a><dl>
<dt><b>TF_IPPMF_FORSESSION</b></dt>
</dl>
</td>
<td width="60%">
Deactivate this profile for all threads in the current desktop.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_DISABLEPROFILE"></a><a id="tf_ippmf_disableprofile"></a><dl>
<dt><b>TF_IPPMF_DISABLEPROFILE</b></dt>
</dl>
</td>
<td width="60%"></td>
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

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofilemgr">ITfInputProcessorProfileMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-activateprofile">ITfInputProcessorProfileMgr::ActivateProfile
      </a>
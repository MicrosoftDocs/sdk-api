---
UID: NF:msctf.ITfInputProcessorProfileMgr.ActivateProfile
title: ITfInputProcessorProfileMgr::ActivateProfile (msctf.h)
description: The ITfInputProcessorProfileMgr::ActivateProfile method activates the specified text service's profile or keyboard layout.
helpviewer_keywords: ["ActivateProfile","ActivateProfile method [Text Services Framework]","ActivateProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","ITfInputProcessorProfileMgr interface [Text Services Framework]","ActivateProfile method","ITfInputProcessorProfileMgr.ActivateProfile","ITfInputProcessorProfileMgr::ActivateProfile","TF_IPPMF_DISABLEPROFILE","TF_IPPMF_DONTCARECURRENTINPUTLANGUAGE","TF_IPPMF_ENABLEPROFILE","TF_IPPMF_FORPROCESS","TF_IPPMF_FORSESSION","TF_PROFILETYPE_INPUTPROCESSOR","TF_PROFILETYPE_KEYBOARDLAYOUT","msctf/ITfInputProcessorProfileMgr::ActivateProfile","tsf.itfinputprocessorprofilemgr_activateprofile"]
old-location: tsf\itfinputprocessorprofilemgr_activateprofile.htm
tech.root: TSF
ms.assetid: 5e5b3f26-332a-456e-875f-12e440ae67ba
ms.date: 12/05/2018
ms.keywords: ActivateProfile, ActivateProfile method [Text Services Framework], ActivateProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, ITfInputProcessorProfileMgr interface [Text Services Framework],ActivateProfile method, ITfInputProcessorProfileMgr.ActivateProfile, ITfInputProcessorProfileMgr::ActivateProfile, TF_IPPMF_DISABLEPROFILE, TF_IPPMF_DONTCARECURRENTINPUTLANGUAGE, TF_IPPMF_ENABLEPROFILE, TF_IPPMF_FORPROCESS, TF_IPPMF_FORSESSION, TF_PROFILETYPE_INPUTPROCESSOR, TF_PROFILETYPE_KEYBOARDLAYOUT, msctf/ITfInputProcessorProfileMgr::ActivateProfile, tsf.itfinputprocessorprofilemgr_activateprofile
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
 - ITfInputProcessorProfileMgr::ActivateProfile
 - msctf/ITfInputProcessorProfileMgr::ActivateProfile
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
 - ITfInputProcessorProfileMgr.ActivateProfile
---

# ITfInputProcessorProfileMgr::ActivateProfile


## -description

The <b>ITfInputProcessorProfileMgr::ActivateProfile</b> method activates the specified text service's profile or keyboard layout.

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

[in] The handle of the keyboard layout. This must be <b>NULL</b> if dwProfileType is TF_PROFILETYPE_INPUTPROCESSOR.

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
Activate this profile for all threads in the process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_FORSESSION"></a><a id="tf_ippmf_forsession"></a><dl>
<dt><b>TF_IPPMF_FORSESSION</b></dt>
</dl>
</td>
<td width="60%">
Activate this profile for all threads in the current desktop.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_ENABLEPROFILE"></a><a id="tf_ippmf_enableprofile"></a><dl>
<dt><b>TF_IPPMF_ENABLEPROFILE</b></dt>
</dl>
</td>
<td width="60%">
Update the registry to enable this profile for this user.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_DISABLEPROFILE"></a><a id="tf_ippmf_disableprofile"></a><dl>
<dt><b>TF_IPPMF_DISABLEPROFILE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="TF_IPPMF_DONTCARECURRENTINPUTLANGUAGE"></a><a id="tf_ippmf_dontcarecurrentinputlanguage"></a><dl>
<dt><b>TF_IPPMF_DONTCARECURRENTINPUTLANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
If the current input language does not match with the requested profile's language, TSF marks this profile to be activated when the requested input language is switched. If this flag is off and the current input language is not matched, this method fails.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The language profile is not enabled.

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



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofilemgr-deactivateprofile">ITfInputProcessorProfileMgr::DeactivateProfile
      </a>
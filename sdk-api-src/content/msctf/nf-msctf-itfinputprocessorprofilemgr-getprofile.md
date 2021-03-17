---
UID: NF:msctf.ITfInputProcessorProfileMgr.GetProfile
title: ITfInputProcessorProfileMgr::GetProfile (msctf.h)
description: The ITfInputProcessorProfileMgr::GetProfile method returns the information of the specified text service's profile or keyboard layout in TF_INPUTPROCESSORPROFILE structure.
helpviewer_keywords: ["GetProfile","GetProfile method [Text Services Framework]","GetProfile method [Text Services Framework]","ITfInputProcessorProfileMgr interface","ITfInputProcessorProfileMgr interface [Text Services Framework]","GetProfile method","ITfInputProcessorProfileMgr.GetProfile","ITfInputProcessorProfileMgr::GetProfile","TF_PROFILETYPE_INPUTPROCESSOR","TF_PROFILETYPE_KEYBOARDLAYOUT","msctf/ITfInputProcessorProfileMgr::GetProfile","tsf.itfinputprocessorprofilemgr_getprofile"]
old-location: tsf\itfinputprocessorprofilemgr_getprofile.htm
tech.root: TSF
ms.assetid: 581bddf5-3def-48c6-a092-4f751142cc1b
ms.date: 12/05/2018
ms.keywords: GetProfile, GetProfile method [Text Services Framework], GetProfile method [Text Services Framework],ITfInputProcessorProfileMgr interface, ITfInputProcessorProfileMgr interface [Text Services Framework],GetProfile method, ITfInputProcessorProfileMgr.GetProfile, ITfInputProcessorProfileMgr::GetProfile, TF_PROFILETYPE_INPUTPROCESSOR, TF_PROFILETYPE_KEYBOARDLAYOUT, msctf/ITfInputProcessorProfileMgr::GetProfile, tsf.itfinputprocessorprofilemgr_getprofile
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
 - ITfInputProcessorProfileMgr::GetProfile
 - msctf/ITfInputProcessorProfileMgr::GetProfile
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
 - ITfInputProcessorProfileMgr.GetProfile
---

# ITfInputProcessorProfileMgr::GetProfile


## -description

The <b>ITfInputProcessorProfileMgr::GetProfile</b> method returns the information of the specified text service's profile or keyboard layout in <a href="/windows/desktop/api/msctf/ns-msctf-tf_inputprocessorprofile">TF_INPUTPROCESSORPROFILE</a> structure.

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

### -param pProfile [out]

[out] The buffer to receive <a href="/windows/desktop/api/msctf/ns-msctf-tf_inputprocessorprofile">TF_INPUTPROCESSORPROFILE</a>.

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
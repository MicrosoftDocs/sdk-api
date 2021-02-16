---
UID: NF:msctf.ITfInputProcessorProfiles.GetActiveLanguageProfile
title: ITfInputProcessorProfiles::GetActiveLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::GetActiveLanguageProfile method
helpviewer_keywords: ["GetActiveLanguageProfile","GetActiveLanguageProfile method [Text Services Framework]","GetActiveLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","GetActiveLanguageProfile method","ITfInputProcessorProfiles.GetActiveLanguageProfile","ITfInputProcessorProfiles::GetActiveLanguageProfile","_tsf_itfinputprocessorprofiles_getactivelanguageprofile_ref","msctf/ITfInputProcessorProfiles::GetActiveLanguageProfile","tsf.itfinputprocessorprofiles_getactivelanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_getactivelanguageprofile.htm
tech.root: TSF
ms.assetid: 446bfda3-63d9-4070-b758-bdaf267c9911
ms.date: 12/05/2018
ms.keywords: GetActiveLanguageProfile, GetActiveLanguageProfile method [Text Services Framework], GetActiveLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetActiveLanguageProfile method, ITfInputProcessorProfiles.GetActiveLanguageProfile, ITfInputProcessorProfiles::GetActiveLanguageProfile, _tsf_itfinputprocessorprofiles_getactivelanguageprofile_ref, msctf/ITfInputProcessorProfiles::GetActiveLanguageProfile, tsf.itfinputprocessorprofiles_getactivelanguageprofile
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfInputProcessorProfiles::GetActiveLanguageProfile
 - msctf/ITfInputProcessorProfiles::GetActiveLanguageProfile
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
 - ITfInputProcessorProfiles.GetActiveLanguageProfile
---

# ITfInputProcessorProfiles::GetActiveLanguageProfile


## -description

Obtains the identifier of the currently active language profile for a specific text service.

## -parameters

### -param rclsid [in]

Contains the text service CLSID.

### -param plangid [out]

Pointer to a <b>LANGID</b> value that receives the active profile language identifier.

### -param pguidProfile [out]

Pointer to a <b>GUID</b> value that receives the language profile identifier. This is the value specified in <a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.

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
The text service identified by <i>rclsid</i> is not currently active. <i>pguidProfile</i> receives GUID_NULL.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
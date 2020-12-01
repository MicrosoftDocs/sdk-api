---
UID: NF:msctf.ITfInputProcessorProfiles.AddLanguageProfile
title: ITfInputProcessorProfiles::AddLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::AddLanguageProfile method
helpviewer_keywords: ["AddLanguageProfile","AddLanguageProfile method [Text Services Framework]","AddLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","AddLanguageProfile method","ITfInputProcessorProfiles.AddLanguageProfile","ITfInputProcessorProfiles::AddLanguageProfile","_tsf_itfinputprocessorprofiles_addlanguageprofile_ref","msctf/ITfInputProcessorProfiles::AddLanguageProfile","tsf.itfinputprocessorprofiles_addlanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_addlanguageprofile.htm
tech.root: TSF
ms.assetid: d132bff1-24de-4e43-859b-2425ba7de8f0
ms.date: 12/05/2018
ms.keywords: AddLanguageProfile, AddLanguageProfile method [Text Services Framework], AddLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],AddLanguageProfile method, ITfInputProcessorProfiles.AddLanguageProfile, ITfInputProcessorProfiles::AddLanguageProfile, _tsf_itfinputprocessorprofiles_addlanguageprofile_ref, msctf/ITfInputProcessorProfiles::AddLanguageProfile, tsf.itfinputprocessorprofiles_addlanguageprofile
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
 - ITfInputProcessorProfiles::AddLanguageProfile
 - msctf/ITfInputProcessorProfiles::AddLanguageProfile
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
 - ITfInputProcessorProfiles.AddLanguageProfile
---

# ITfInputProcessorProfiles::AddLanguageProfile


## -description

Creates a language profile that consists of a specific text service and a specific language identifier.

## -parameters

### -param rclsid [in]

Contains the text service CLSID.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language identifier of the profile that the text service is added to. If this contains -1, the text service is added to all languages.

### -param guidProfile [in]

Contains a GUID value that identifies the language profile. This is the value obtained by <a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getactivelanguageprofile">ITfInputProcessorProfiles::GetActiveLanguageProfile</a> when the profile is active.

### -param pchDesc [in]

Pointer to a <b>WCHAR</b> buffer that contains the description string for the text service in the profile. This is the text service name displayed in the language bar.

### -param cchDesc [in]

Contains the length, in characters, of the description string in <i>pchDesc</i>. If this contains -1, <i>pchDesc</i> is assumed to be a <b>NULL</b>-terminated string.

### -param pchIconFile [in]

Pointer to a <b>WCHAR</b> buffer that contains the path and file name of the file that contains the icon to be displayed in the language bar for the text service in the profile. This file can be an executable (.exe), DLL (.dll) or icon (.ico) file.

This parameter is optional and can be <b>NULL</b>. In this case, a default icon is displayed for the text service.

### -param cchFile [in]

Contains the length, in characters, of the icon file string in <i>pchIconFile</i>. If this contains -1, <i>pchIconFile</i> is assumed to be a <b>NULL</b>-terminated string. This parameter is ignored if <i>pchIconFile</i> is <b>NULL</b>.

### -param uIconIndex [in]

Contains the zero-based index of the icon in <i>pchIconFile</i> to be displayed in the language bar for the text service in the profile. This parameter is ignored if <i>pchIconFile</i> is <b>NULL</b>.

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
<i>pszDesc</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-getactivelanguageprofile">ITfInputProcessorProfiles::GetActiveLanguageProfile
      </a>
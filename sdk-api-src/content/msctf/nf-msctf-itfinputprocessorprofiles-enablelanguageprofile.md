---
UID: NF:msctf.ITfInputProcessorProfiles.EnableLanguageProfile
title: ITfInputProcessorProfiles::EnableLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::EnableLanguageProfile method
helpviewer_keywords: ["EnableLanguageProfile","EnableLanguageProfile method [Text Services Framework]","EnableLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","EnableLanguageProfile method","ITfInputProcessorProfiles.EnableLanguageProfile","ITfInputProcessorProfiles::EnableLanguageProfile","_tsf_itfinputprocessorprofiles_enablelanguageprofile_ref","msctf/ITfInputProcessorProfiles::EnableLanguageProfile","tsf.itfinputprocessorprofiles_enablelanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_enablelanguageprofile.htm
tech.root: TSF
ms.assetid: 54aa6668-e577-4d75-9461-b604e1e73a78
ms.date: 12/05/2018
ms.keywords: EnableLanguageProfile, EnableLanguageProfile method [Text Services Framework], EnableLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],EnableLanguageProfile method, ITfInputProcessorProfiles.EnableLanguageProfile, ITfInputProcessorProfiles::EnableLanguageProfile, _tsf_itfinputprocessorprofiles_enablelanguageprofile_ref, msctf/ITfInputProcessorProfiles::EnableLanguageProfile, tsf.itfinputprocessorprofiles_enablelanguageprofile
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
 - ITfInputProcessorProfiles::EnableLanguageProfile
 - msctf/ITfInputProcessorProfiles::EnableLanguageProfile
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
 - ITfInputProcessorProfiles.EnableLanguageProfile
---

# ITfInputProcessorProfiles::EnableLanguageProfile


## -description

Enables or disables a language profile for the current user.

## -parameters

### -param rclsid [in]

Contains the CLSID of the text service of the profile to be enabled or disabled.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language of the profile to be enabled or disabled.

### -param guidProfile [in]

Contains a GUID value that identifies the profile to be enabled or disabled.

### -param fEnable [in]

Contains a <b>BOOL</b> value that specifies if the profile will be enabled or disabled. If this contains a nonzero value, the profile will be enabled. If this contains zero, the profile will be disabled.

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
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-enablelanguageprofilebydefault">ITfInputProcessorProfiles::EnableLanguageProfileByDefault
      </a>
---
UID: NF:msctf.ITfInputProcessorProfiles.RemoveLanguageProfile
title: ITfInputProcessorProfiles::RemoveLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::RemoveLanguageProfile method
helpviewer_keywords: ["ITfInputProcessorProfiles interface [Text Services Framework]","RemoveLanguageProfile method","ITfInputProcessorProfiles.RemoveLanguageProfile","ITfInputProcessorProfiles::RemoveLanguageProfile","RemoveLanguageProfile","RemoveLanguageProfile method [Text Services Framework]","RemoveLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","_tsf_itfinputprocessorprofiles_removelanguageprofile_ref","msctf/ITfInputProcessorProfiles::RemoveLanguageProfile","tsf.itfinputprocessorprofiles_removelanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_removelanguageprofile.htm
tech.root: TSF
ms.assetid: 16eff9bc-1789-4bf6-b1ba-b7e8414ce080
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],RemoveLanguageProfile method, ITfInputProcessorProfiles.RemoveLanguageProfile, ITfInputProcessorProfiles::RemoveLanguageProfile, RemoveLanguageProfile, RemoveLanguageProfile method [Text Services Framework], RemoveLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_removelanguageprofile_ref, msctf/ITfInputProcessorProfiles::RemoveLanguageProfile, tsf.itfinputprocessorprofiles_removelanguageprofile
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
 - ITfInputProcessorProfiles::RemoveLanguageProfile
 - msctf/ITfInputProcessorProfiles::RemoveLanguageProfile
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
 - ITfInputProcessorProfiles.RemoveLanguageProfile
---

# ITfInputProcessorProfiles::RemoveLanguageProfile


## -description

Removes a language profile.

## -parameters

### -param rclsid [in]

Contains the text service CLSID.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language identifier of the profile.

### -param guidProfile [out]

Contains a GUID value that identifies the language profile. This is the value specified in <a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.

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



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
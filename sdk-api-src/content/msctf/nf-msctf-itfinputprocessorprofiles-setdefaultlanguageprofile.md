---
UID: NF:msctf.ITfInputProcessorProfiles.SetDefaultLanguageProfile
title: ITfInputProcessorProfiles::SetDefaultLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::SetDefaultLanguageProfile method
helpviewer_keywords: ["ITfInputProcessorProfiles interface [Text Services Framework]","SetDefaultLanguageProfile method","ITfInputProcessorProfiles.SetDefaultLanguageProfile","ITfInputProcessorProfiles::SetDefaultLanguageProfile","SetDefaultLanguageProfile","SetDefaultLanguageProfile method [Text Services Framework]","SetDefaultLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","_tsf_itfinputprocessorprofiles_setdefaultlanguageprofile_ref","msctf/ITfInputProcessorProfiles::SetDefaultLanguageProfile","tsf.itfinputprocessorprofiles_setdefaultlanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_setdefaultlanguageprofile.htm
tech.root: TSF
ms.assetid: 385bf5d6-6541-483d-8286-1ba759616fc6
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],SetDefaultLanguageProfile method, ITfInputProcessorProfiles.SetDefaultLanguageProfile, ITfInputProcessorProfiles::SetDefaultLanguageProfile, SetDefaultLanguageProfile, SetDefaultLanguageProfile method [Text Services Framework], SetDefaultLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_setdefaultlanguageprofile_ref, msctf/ITfInputProcessorProfiles::SetDefaultLanguageProfile, tsf.itfinputprocessorprofiles_setdefaultlanguageprofile
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
 - ITfInputProcessorProfiles::SetDefaultLanguageProfile
 - msctf/ITfInputProcessorProfiles::SetDefaultLanguageProfile
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
 - ITfInputProcessorProfiles.SetDefaultLanguageProfile
---

# ITfInputProcessorProfiles::SetDefaultLanguageProfile


## -description

Sets the default profile for a specific language.

## -parameters

### -param langid [in]

Contains a LANGID value that specifies which language to set the default profile for.

### -param rclsid [in]

Contains the CLSID of the text service that will be the default for the language.

### -param guidProfiles [in]

Contains a GUID value that identifies the language profile that will be the default.

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


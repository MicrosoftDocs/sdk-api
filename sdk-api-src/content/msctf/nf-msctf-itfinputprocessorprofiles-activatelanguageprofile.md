---
UID: NF:msctf.ITfInputProcessorProfiles.ActivateLanguageProfile
title: ITfInputProcessorProfiles::ActivateLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::ActivateLanguageProfile method
helpviewer_keywords: ["ActivateLanguageProfile","ActivateLanguageProfile method [Text Services Framework]","ActivateLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","ActivateLanguageProfile method","ITfInputProcessorProfiles.ActivateLanguageProfile","ITfInputProcessorProfiles::ActivateLanguageProfile","_tsf_itfinputprocessorprofiles_activatelanguageprofile_ref","msctf/ITfInputProcessorProfiles::ActivateLanguageProfile","tsf.itfinputprocessorprofiles_activatelanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_activatelanguageprofile.htm
tech.root: TSF
ms.assetid: d25e5a11-8394-4fc5-b210-afa753223307
ms.date: 12/05/2018
ms.keywords: ActivateLanguageProfile, ActivateLanguageProfile method [Text Services Framework], ActivateLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],ActivateLanguageProfile method, ITfInputProcessorProfiles.ActivateLanguageProfile, ITfInputProcessorProfiles::ActivateLanguageProfile, _tsf_itfinputprocessorprofiles_activatelanguageprofile_ref, msctf/ITfInputProcessorProfiles::ActivateLanguageProfile, tsf.itfinputprocessorprofiles_activatelanguageprofile
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
 - ITfInputProcessorProfiles::ActivateLanguageProfile
 - msctf/ITfInputProcessorProfiles::ActivateLanguageProfile
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
 - ITfInputProcessorProfiles.ActivateLanguageProfile
---

# ITfInputProcessorProfiles::ActivateLanguageProfile


## -description

Sets the active text service for a specific language.

## -parameters

Sets the active text service for a specific language.

### -param rclsid [in]

Contains the CLSID of the text service to make active.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies which language to set the default profile for. This method fails if this is not the currently active language.

### -param guidProfiles [in]

Contains a GUID value that identifies the language profile to make active.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No thread manager has been created for the calling thread.

</td>
</tr>
</table>


---
UID: NF:msctf.ITfInputProcessorProfiles.GetDefaultLanguageProfile
title: ITfInputProcessorProfiles::GetDefaultLanguageProfile (msctf.h)
description: ITfInputProcessorProfiles::GetDefaultLanguageProfile method
helpviewer_keywords: ["GetDefaultLanguageProfile","GetDefaultLanguageProfile method [Text Services Framework]","GetDefaultLanguageProfile method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","GetDefaultLanguageProfile method","ITfInputProcessorProfiles.GetDefaultLanguageProfile","ITfInputProcessorProfiles::GetDefaultLanguageProfile","_tsf_itfinputprocessorprofiles_getdefaultlanguageprofile_ref","msctf/ITfInputProcessorProfiles::GetDefaultLanguageProfile","tsf.itfinputprocessorprofiles_getdefaultlanguageprofile"]
old-location: tsf\itfinputprocessorprofiles_getdefaultlanguageprofile.htm
tech.root: TSF
ms.assetid: a846505e-d6d5-4462-b420-f36fd2051d92
ms.date: 12/05/2018
ms.keywords: GetDefaultLanguageProfile, GetDefaultLanguageProfile method [Text Services Framework], GetDefaultLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetDefaultLanguageProfile method, ITfInputProcessorProfiles.GetDefaultLanguageProfile, ITfInputProcessorProfiles::GetDefaultLanguageProfile, _tsf_itfinputprocessorprofiles_getdefaultlanguageprofile_ref, msctf/ITfInputProcessorProfiles::GetDefaultLanguageProfile, tsf.itfinputprocessorprofiles_getdefaultlanguageprofile
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
 - ITfInputProcessorProfiles::GetDefaultLanguageProfile
 - msctf/ITfInputProcessorProfiles::GetDefaultLanguageProfile
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
 - ITfInputProcessorProfiles.GetDefaultLanguageProfile
---

# ITfInputProcessorProfiles::GetDefaultLanguageProfile


## -description

Obtains the default profile for a specific language.

## -parameters

### -param langid [in]

Contains a <b>LANGID</b> value that specifies which language to obtain the default profile for.

### -param catid [in]

Contains a GUID value that identifies the category that the text service is registered under. This can be a user-defined category or one of the <a href="/windows/desktop/TSF/predefined-category-values">predefined category values</a>.

### -param pclsid [out]

Pointer to a <b>CLSID</b> value that receives the class identifier of the default text service for the language.

### -param pguidProfile [out]

Pointer to a <b>GUID</b> value that receives the identifier of the default profile for the language.

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
No default language profile was found for the specified language and category.

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

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/TSF/predefined-category-values">Predefined Category Values
      </a>
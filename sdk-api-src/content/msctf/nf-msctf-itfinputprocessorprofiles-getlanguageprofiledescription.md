---
UID: NF:msctf.ITfInputProcessorProfiles.GetLanguageProfileDescription
title: ITfInputProcessorProfiles::GetLanguageProfileDescription (msctf.h)
description: ITfInputProcessorProfiles::GetLanguageProfileDescription method
helpviewer_keywords: ["GetLanguageProfileDescription","GetLanguageProfileDescription method [Text Services Framework]","GetLanguageProfileDescription method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","GetLanguageProfileDescription method","ITfInputProcessorProfiles.GetLanguageProfileDescription","ITfInputProcessorProfiles::GetLanguageProfileDescription","_tsf_itfinputprocessorprofiles_getlanguageprofiledescription_ref","msctf/ITfInputProcessorProfiles::GetLanguageProfileDescription","tsf.itfinputprocessorprofiles_getlanguageprofiledescription"]
old-location: tsf\itfinputprocessorprofiles_getlanguageprofiledescription.htm
tech.root: TSF
ms.assetid: f5838d26-1065-498c-8361-8929c07fc725
ms.date: 12/05/2018
ms.keywords: GetLanguageProfileDescription, GetLanguageProfileDescription method [Text Services Framework], GetLanguageProfileDescription method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetLanguageProfileDescription method, ITfInputProcessorProfiles.GetLanguageProfileDescription, ITfInputProcessorProfiles::GetLanguageProfileDescription, _tsf_itfinputprocessorprofiles_getlanguageprofiledescription_ref, msctf/ITfInputProcessorProfiles::GetLanguageProfileDescription, tsf.itfinputprocessorprofiles_getlanguageprofiledescription
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
 - ITfInputProcessorProfiles::GetLanguageProfileDescription
 - msctf/ITfInputProcessorProfiles::GetLanguageProfileDescription
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
 - ITfInputProcessorProfiles.GetLanguageProfileDescription
---

# ITfInputProcessorProfiles::GetLanguageProfileDescription


## -description

Obtains the description string for a language profile.

## -parameters

### -param rclsid [in]

Contains the CLSID of the text service to obtain the profile description for.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies which language to obtain the profile description for.

### -param guidProfile [in]

Contains a GUID value that identifies the language to obtain the profile description for.

### -param pbstrProfile [out]

Pointer to a <b>BSTR</b> value that receives the description string. The caller is responsible for freeing this memory using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

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
<i>pbstrProfile</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile
      </a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
---
UID: NF:msctf.ITfInputProcessorProfiles.GetCurrentLanguage
title: ITfInputProcessorProfiles::GetCurrentLanguage (msctf.h)
description: ITfInputProcessorProfiles::GetCurrentLanguage method
helpviewer_keywords: ["GetCurrentLanguage","GetCurrentLanguage method [Text Services Framework]","GetCurrentLanguage method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","GetCurrentLanguage method","ITfInputProcessorProfiles.GetCurrentLanguage","ITfInputProcessorProfiles::GetCurrentLanguage","_tsf_itfinputprocessorprofiles_getcurrentlanguage_ref","msctf/ITfInputProcessorProfiles::GetCurrentLanguage","tsf.itfinputprocessorprofiles_getcurrentlanguage"]
old-location: tsf\itfinputprocessorprofiles_getcurrentlanguage.htm
tech.root: TSF
ms.assetid: c770872f-752f-4c34-8d0d-cdf3d5c7d6b4
ms.date: 12/05/2018
ms.keywords: GetCurrentLanguage, GetCurrentLanguage method [Text Services Framework], GetCurrentLanguage method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetCurrentLanguage method, ITfInputProcessorProfiles.GetCurrentLanguage, ITfInputProcessorProfiles::GetCurrentLanguage, _tsf_itfinputprocessorprofiles_getcurrentlanguage_ref, msctf/ITfInputProcessorProfiles::GetCurrentLanguage, tsf.itfinputprocessorprofiles_getcurrentlanguage
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
 - ITfInputProcessorProfiles::GetCurrentLanguage
 - msctf/ITfInputProcessorProfiles::GetCurrentLanguage
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
 - ITfInputProcessorProfiles.GetCurrentLanguage
---

# ITfInputProcessorProfiles::GetCurrentLanguage


## -description

Obtains the identifier of the currently active language.

## -parameters

### -param plangid [out]

Pointer to a <b>LANGID</b> value that receives the language identifier of the currently active language.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>plangid</i> is invalid.

</td>
</tr>
</table>


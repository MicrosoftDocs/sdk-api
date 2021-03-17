---
UID: NF:msctf.ITfInputProcessorProfiles.GetLanguageList
title: ITfInputProcessorProfiles::GetLanguageList (msctf.h)
description: ITfInputProcessorProfiles::GetLanguageList method
helpviewer_keywords: ["GetLanguageList","GetLanguageList method [Text Services Framework]","GetLanguageList method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","GetLanguageList method","ITfInputProcessorProfiles.GetLanguageList","ITfInputProcessorProfiles::GetLanguageList","_tsf_itfinputprocessorprofiles_getlanguagelist_ref","msctf/ITfInputProcessorProfiles::GetLanguageList","tsf.itfinputprocessorprofiles_getlanguagelist"]
old-location: tsf\itfinputprocessorprofiles_getlanguagelist.htm
tech.root: TSF
ms.assetid: dffca277-1c2c-4e3d-965f-42e7907ba603
ms.date: 12/05/2018
ms.keywords: GetLanguageList, GetLanguageList method [Text Services Framework], GetLanguageList method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetLanguageList method, ITfInputProcessorProfiles.GetLanguageList, ITfInputProcessorProfiles::GetLanguageList, _tsf_itfinputprocessorprofiles_getlanguagelist_ref, msctf/ITfInputProcessorProfiles::GetLanguageList, tsf.itfinputprocessorprofiles_getlanguagelist
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
 - ITfInputProcessorProfiles::GetLanguageList
 - msctf/ITfInputProcessorProfiles::GetLanguageList
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
 - ITfInputProcessorProfiles.GetLanguageList
---

# ITfInputProcessorProfiles::GetLanguageList


## -description

Obtains a list of the installed languages.

## -parameters

### -param ppLangId [out]

Pointer to a <b>LANGID</b> pointer that receives the array of identifiers of the currently installed languages. The number of identifiers placed in this array is supplied in <i>pulCount</i>. The array is allocated by this method. The caller must free this memory when it is no longer required using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pulCount [out]

Pointer to a ULONG value the receives the number of identifiers placed in the array at <i>ppLangId</i>.

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
</table>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>